# Parte III — Integração e Referências

## Integração com o Cadastro de Pessoas

O SIAD Benefícios é integrado nativamente ao cadastro de pessoas do SIAD. Todo beneficiário é obrigatoriamente vinculado a uma pessoa existente no sistema, e o perfil da pessoa consolida todos os benefícios recebidos em uma visão unificada.

### Benefícios no perfil da pessoa

No módulo de Atendimento, ao acessar o cadastro de uma pessoa, o menu lateral exibe o item **"Benefícios"** (visível para usuários com permissão `PESSOA_BENEFICIOS_ACESSAR`). Esse item possui um **badge** com a contagem total de benefícios ativos da pessoa.

A página exibe em uma única interface:

1. **Benefícios - Cadastro de Pessoas**: lista de benefícios socioassistenciais e previdenciários registrados diretamente no cadastro da pessoa (Programa Geração de Renda, Programa Transcidadania, entre outros).
2. **SIAD Benefícios**: tabela com todos os benefícios dinâmicos em que a pessoa está cadastrada, com colunas de benefício, status, equipamento e links de visualização que levam diretamente ao módulo de Benefícios.

### Cadastro rápido a partir do perfil da pessoa

Na tela de benefícios da pessoa, o botão **"Cadastrar Benefício"** redireciona o técnico para o formulário de criação do SIAD Benefícios com o parâmetro `?pessoa_id=X` na URL. Isso faz com que o campo **Pessoa** já venha pré-preenchido e bloqueado, agilizando o cadastro.

O fluxo fica:

1. Técnico acessa o perfil da pessoa no módulo de Atendimento
2. Navega até a aba "Benefícios"
3. Clica em "Cadastrar Benefício"
4. É redirecionado ao formulário com a pessoa já selecionada
5. Seleciona o benefício, equipamento, status e preenche o formulário dinâmico
6. Salva

### Link "Ir para o Cadastro da Pessoa"

No caminho inverso, ao visualizar um beneficiário dentro do SIAD Benefícios, a **sidebar lateral** exibe o link **"Ir para o Cadastro da Pessoa"** que abre o perfil completo da pessoa no módulo de Atendimento (em nova aba se aplicável).

Isso facilita a navegação quando o técnico precisa:

* Consultar dados pessoais completos (endereço, composição familiar etc.)
* Verificar outros benefícios que a pessoa recebe
* Acessar o histórico de atendimentos

### Validação de duplicidade

O sistema impede que a mesma pessoa seja cadastrada duas vezes no mesmo benefício. Ao tentar, a validação exibe:

> _"Esta pessoa já está cadastrada neste benefício."_

Essa regra garante integridade dos dados e evita duplicações operacionais. Caso a pessoa tenha sido desligada e precise ser recadastrada, é necessário excluir o cadastro anterior (ou restaurá-lo e alterar o status).

### Resumo da integração

| Ação                                      | Origem                                                     | Destino                                                          |
| ----------------------------------------- | ---------------------------------------------------------- | ---------------------------------------------------------------- |
| Cadastrar benefício a partir da pessoa    | Perfil da pessoa > Benefícios > "Cadastrar Benefício"      | Formulário de criação no SIAD Benefícios (pessoa pré-preenchida) |
| Consultar pessoa a partir do beneficiário | SIAD Benefícios > Sidebar > "Ir para o Cadastro da Pessoa" | Perfil completo da pessoa no Atendimento                         |
| Ver todos os benefícios de uma pessoa     | Perfil da pessoa > Benefícios                              | Lista unificada (cadastros tradicionais + SIAD Benefícios)       |

***

## Permissões — Referência Completa

Esta página consolida todas as permissões do módulo de Benefícios em formato de referência rápida. As permissões são geradas automaticamente para cada benefício criado e seguem o padrão `PREFIXO_{ID}_AÇÃO`.

### Permissões globais (independem de benefício específico)

Estas permissões controlam o acesso geral ao módulo:

<table><thead><tr><th width="354">Permissão</th><th>Descrição</th></tr></thead><tbody><tr><td><code>BENEFICIOS_ACESSAR</code></td><td>Acesso ao menu de configurações de benefícios</td></tr><tr><td><code>BENEFICIOS_CADASTRAR</code></td><td>Criar novos benefícios (também permite ver benefícios em rascunho na listagem)</td></tr><tr><td><code>BENEFICIARIOS_ACESSAR</code></td><td>Pré-requisito global para acessar a listagem de beneficiários</td></tr><tr><td><code>BENEFICIARIOS_CADASTRAR</code></td><td>Pré-requisito global para o botão de cadastrar beneficiários</td></tr><tr><td><code>BENEFICIARIOS_ACESSAR_GLOBAL</code></td><td>Visualizar cadastros de todos os benefícios, ignorando vínculos de equipamento</td></tr><tr><td><code>BENEFICIARIOS_ACOMPANHAMENTO_ACESSAR</code></td><td>Acessar o painel gerencial de acompanhamento (menu Benefícios > Acompanhamento)</td></tr></tbody></table>

### Permissões por benefício — Configuração

Prefixo: `BENEFICIO_{ID}_`

| Sufixo                 | Descrição                                    | Perfil típico |
| ---------------------- | -------------------------------------------- | ------------- |
| `CONSULTAR`            | Visualizar as configurações do benefício     | Gestor        |
| `ALTERAR`              | Editar configurações, formulários e vínculos | Gestor        |
| `EXCLUIR`              | Excluir o benefício                          | Administrador |
| `REATIVAR`             | Restaurar benefício excluído                 | Administrador |
| `CONFIGURACOES_GERAIS` | Acessar configurações gerais avançadas       | Gestor        |

### Permissões por benefício — Operação de cadastros

Prefixo: `BENEFICIARIOS_{ID}_`

<table><thead><tr><th width="186.333251953125">Sufixo</th><th width="403.333251953125">Descrição</th><th>Perfil típico</th></tr></thead><tbody><tr><td><code>ACESSAR</code></td><td>Ver a aba do benefício na listagem. <strong>Essencial</strong> — sem ela o benefício fica invisível.</td><td>Técnico</td></tr><tr><td><code>CADASTRAR</code></td><td>Inserir novo beneficiário (restrito ao seu equipamento)</td><td>Técnico</td></tr><tr><td><code>CONSULTAR</code></td><td>Visualizar dados dos cadastros</td><td>Técnico</td></tr><tr><td><code>ALTERAR</code></td><td>Editar formulário e status dos cadastros</td><td>Técnico</td></tr><tr><td><code>EXCLUIR</code></td><td>Excluir cadastros (soft delete)</td><td>Coordenador</td></tr><tr><td><code>REATIVAR</code></td><td>Restaurar cadastros excluídos</td><td>Coordenador</td></tr><tr><td><code>ACESSAR_GLOBAL</code></td><td>Ignora restrição de equipamento — vê cadastros de toda a rede</td><td>Supervisor</td></tr><tr><td><code>CADASTRAR_GLOBAL</code></td><td>Desbloqueia campo de equipamento — pode cadastrar em qualquer equipamento</td><td>Supervisor</td></tr></tbody></table>

### Permissões por benefício — Acompanhamento

Prefixo: `BENEFICIARIOS_{ID}_ACOMPANHAMENTO_`

<table><thead><tr><th width="193.666748046875">Sufixo</th><th width="396.333251953125">Descrição</th><th>Perfil típico</th></tr></thead><tbody><tr><td><code>ACESSAR</code></td><td>Ver a aba/botão de acompanhamento no cadastro</td><td>Técnico</td></tr><tr><td><code>CADASTRAR</code></td><td>Registrar acompanhamentos (restrito ao equipamento do cadastro)</td><td>Técnico</td></tr><tr><td><code>CADASTRAR_GLOBAL</code></td><td>Registrar para beneficiários de qualquer equipamento</td><td>Supervisor</td></tr><tr><td><code>CONSULTAR</code></td><td>Visualizar acompanhamentos existentes</td><td>Técnico</td></tr><tr><td><code>ALTERAR</code></td><td>Editar acompanhamentos já registrados</td><td>Técnico</td></tr><tr><td><code>EXCLUIR</code></td><td>Excluir acompanhamentos</td><td>Coordenador</td></tr></tbody></table>

### Permissões por benefício — Administração de equipamentos

Prefixo: `BENEFICIARIOS_{ID}_EQUIPAMENTOS_`

<table><thead><tr><th width="145">Sufixo</th><th width="408.3333740234375">Descrição</th><th>Perfil típico</th></tr></thead><tbody><tr><td><code>ACESSAR</code></td><td>Ver a tela de configuração de equipamentos</td><td>Gestor</td></tr><tr><td><code>CADASTRAR</code></td><td>Vincular novos equipamentos ao benefício</td><td>Gestor</td></tr><tr><td><code>EXCLUIR</code></td><td>Desvincular equipamentos</td><td>Gestor</td></tr></tbody></table>

### Permissões por benefício — Administração de organizações

Prefixo: `BENEFICIARIOS_{ID}_ORGANIZACOES_`

<table><thead><tr><th width="148.3333740234375">Sufixo</th><th width="418.3333740234375">Descrição</th><th>Perfil típico</th></tr></thead><tbody><tr><td><code>ACESSAR</code></td><td>Ver a tela de configuração de organizações</td><td>Gestor</td></tr><tr><td><code>CADASTRAR</code></td><td>Vincular novas organizações ao benefício</td><td>Gestor</td></tr><tr><td><code>EXCLUIR</code></td><td>Desvincular organizações</td><td>Gestor</td></tr></tbody></table>

### Permissões por benefício — Gerenciamento de permissões

Prefixo: `BENEFICIARIOS_{ID}_PERMISSOES_`

<table><thead><tr><th width="139.666748046875">Sufixo</th><th width="426">Descrição</th><th>Perfil típico</th></tr></thead><tbody><tr><td><code>ACESSAR</code></td><td>Ver a tela que lista todas as permissões geradas</td><td>Gestor</td></tr><tr><td><code>CADASTRAR</code></td><td>Gerar permissões faltantes</td><td>Gestor</td></tr><tr><td><code>EXCLUIR</code></td><td>Remover permissões</td><td>Administrador</td></tr></tbody></table>

### Perfis sugeridos

#### Técnico operacional

Permissões mínimas para operar o dia-a-dia:

```
BENEFICIARIOS_ACESSAR
BENEFICIARIOS_CADASTRAR
BENEFICIARIOS_{ID}_ACESSAR
BENEFICIARIOS_{ID}_CADASTRAR
BENEFICIARIOS_{ID}_CONSULTAR
BENEFICIARIOS_{ID}_ALTERAR
BENEFICIARIOS_{ID}_ACOMPANHAMENTO_ACESSAR
BENEFICIARIOS_{ID}_ACOMPANHAMENTO_CADASTRAR
BENEFICIARIOS_{ID}_ACOMPANHAMENTO_CONSULTAR
```

#### Coordenador / Supervisor

Todas as do técnico, mais:

```
BENEFICIARIOS_{ID}_ACESSAR_GLOBAL
BENEFICIARIOS_{ID}_CADASTRAR_GLOBAL
BENEFICIARIOS_{ID}_ACOMPANHAMENTO_CADASTRAR_GLOBAL
BENEFICIARIOS_{ID}_EXCLUIR
BENEFICIARIOS_{ID}_REATIVAR
BENEFICIARIOS_{ID}_ACOMPANHAMENTO_ALTERAR
BENEFICIARIOS_{ID}_ACOMPANHAMENTO_EXCLUIR
BENEFICIARIOS_ACOMPANHAMENTO_ACESSAR
```

#### Gestor de configuração

Permissões para criar e manter o benefício:

```
BENEFICIOS_ACESSAR
BENEFICIOS_CADASTRAR
BENEFICIO_{ID}_CONSULTAR
BENEFICIO_{ID}_ALTERAR
BENEFICIO_{ID}_CONFIGURACOES_GERAIS
BENEFICIARIOS_{ID}_EQUIPAMENTOS_ACESSAR
BENEFICIARIOS_{ID}_EQUIPAMENTOS_CADASTRAR
BENEFICIARIOS_{ID}_EQUIPAMENTOS_EXCLUIR
BENEFICIARIOS_{ID}_ORGANIZACOES_ACESSAR
BENEFICIARIOS_{ID}_ORGANIZACOES_CADASTRAR
BENEFICIARIOS_{ID}_ORGANIZACOES_EXCLUIR
BENEFICIARIOS_{ID}_PERMISSOES_ACESSAR
BENEFICIARIOS_{ID}_PERMISSOES_CADASTRAR
```

### Regras de combinação

Algumas regras importantes sobre como as permissões interagem:

* A permissão `ACESSAR` é pré-requisito para todas as demais — sem ela, nenhuma outra tem efeito visível.
* As permissões `GLOBAL` **não substituem** as permissões base — o usuário precisa ter ambas. Ex: `ACESSAR_GLOBAL` sem `ACESSAR` não funciona.
* O vínculo de equipamento é validado independentemente: mesmo com `ACESSAR`, se o equipamento do técnico não estiver vinculado ao benefício, a aba não aparecerá (exceto com `ACESSAR_GLOBAL`).
* Permissões do perfil **Administrador** do sistema são atribuídas automaticamente a todas as permissões geradas — não é necessário configurar manualmente.
