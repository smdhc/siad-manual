# Parte I — Configuração (perfil gestor)

## Criar um Benefício

Para criar um novo benefício, acesse o menu lateral **Benefícios > Configurações** e clique em **Novo Benefício**.

O formulário de criação está dividido em três seções: Informações Gerais, Configuração de Formulários e Outros.

### Informações Gerais

<table><thead><tr><th width="175">Campo</th><th width="127.3333740234375" align="center">Obrigatório</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Nome do Benefício</strong></td><td align="center">Sim</td><td>Nome identificador do benefício. Será exibido nas abas de cadastro, nos filtros e em todas as referências ao benefício no sistema. Ex: "Auxílio Aluguel", "POT Esporte".</td></tr><tr><td><strong>Status</strong></td><td align="center">Sim</td><td>Define a disponibilidade do benefício. Ao criar, use <strong>Rascunho</strong> até finalizar toda a configuração. Somente benefícios com status <strong>Publicado</strong> ficam acessíveis para cadastro de beneficiários.</td></tr><tr><td><strong>Descrição</strong></td><td align="center">Não</td><td>Texto livre para documentar o objetivo, público-alvo ou regras gerais do benefício. Visível apenas na área de configuração.</td></tr></tbody></table>

### Configuração de Formulários e Status

<table><thead><tr><th width="221">Campo</th><th width="122.3333740234375" align="center">Obrigatório</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Formulário de Cadastro</strong></td><td align="center">Não</td><td>Selecione o formulário que será preenchido ao cadastrar uma pessoa no benefício. Somente formulários com pelo menos uma versão publicada são listados.</td></tr><tr><td><strong>Versão de Cadastro</strong></td><td align="center">Condicional</td><td>Selecione a versão publicada do formulário de cadastro. Obrigatório quando um formulário estiver selecionado.</td></tr><tr><td><strong>Status permitidos</strong></td><td align="center">Sim</td><td>Lista de status que os cadastros deste benefício poderão assumir. Digite cada status e pressione Enter para adicionar. Ex: "Ativo", "Inativo", "Em Análise", "Desligado". É possível reordenar arrastando.</td></tr></tbody></table>

Os **status permitidos** são fundamentais para a operação do benefício. Eles permitem:

* Classificar os beneficiários por situação atual
* Filtrar cadastros na listagem
* Definir quais status são considerados "ativos" para fins de controle de pendências de acompanhamento

> **Dica**: pense nos status como o ciclo de vida do beneficiário dentro do programa. Um fluxo típico pode ser: "Em Análise" → "Ativo" → "Desligado".

### Configuração de Acompanhamento

O acompanhamento é **opcional**. Ative o toggle **"Habilitar acompanhamento?"** caso o benefício exija registro periódico de informações sobre os beneficiários.

Ao ativar, os seguintes campos ficam disponíveis:

<table><thead><tr><th width="170.333251953125">Campo</th><th width="123.3333740234375" align="center">Obrigatório</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Periodicidade</strong></td><td align="center">Sim</td><td>Define a frequência dos acompanhamentos. Opções: Mensal, Bimestral, Trimestral, Semestral, Anual. A periodicidade determina as opções de referência (Janeiro/Fevereiro... ou 1º Bimestre/2º Bimestre... etc.).</td></tr><tr><td><strong>Status Ativo</strong></td><td align="center">Sim</td><td>Selecione quais dos status permitidos são considerados "ativos". Apenas beneficiários com esses status aparecerão na tabela de pendências de acompanhamento. Ex: marcar "Ativo" e "Em Acompanhamento".</td></tr><tr><td><strong>Formulário de Acompanhamento</strong></td><td align="center">Sim</td><td>Selecione o formulário que será preenchido a cada registro de acompanhamento. Deve ter versão publicada.</td></tr><tr><td><strong>Versão de Acompanhamento</strong></td><td align="center">Sim</td><td>Selecione a versão publicada do formulário de acompanhamento.</td></tr></tbody></table>

### Vínculos com Equipamento e Organização

A seção **Outros** configura como o benefício se relaciona com equipamentos (CRAS, CREAS etc.) e organizações parceiras.

#### Equipamento

<table><thead><tr><th width="249.333251953125">Campo</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Habilitar Equipamento</strong></td><td>Quando ativo, permite vincular equipamentos ao benefício. Técnicos só verão cadastros do benefício se seu equipamento estiver vinculado (exceto usuários com acesso global). Padrão: ativo.</td></tr><tr><td><strong>Obrigatório?</strong></td><td>Torna obrigatória a seleção de um equipamento ao cadastrar um beneficiário.</td></tr><tr><td><strong>Exibir equipamento logado por padrão</strong></td><td>Pré-preenche o campo de equipamento com o equipamento do usuário logado.</td></tr><tr><td><strong>Bloquear edição</strong></td><td>Visível quando "Exibir equipamento logado por padrão" está ativo. Impede que o técnico altere o equipamento — ele fica travado no equipamento do usuário. Usuários com permissão <code>CADASTRAR_GLOBAL</code> podem sobrescrever esse bloqueio.</td></tr></tbody></table>

#### Organização

<table><thead><tr><th width="248.6666259765625">Campo</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Habilitar Organização</strong></td><td>Quando ativo, permite vincular organizações parceiras ao benefício. Padrão: desativado.</td></tr><tr><td><strong>Obrigatório?</strong></td><td>Torna obrigatória a seleção de uma organização ao cadastrar um beneficiário.</td></tr><tr><td><strong>Exibir organização logada por padrão</strong></td><td>Pré-preenche o campo com a organização do usuário logado.</td></tr><tr><td><strong>Bloquear edição</strong></td><td>Mesma lógica do equipamento — trava o campo com a organização do usuário logado.</td></tr></tbody></table>

### Campos adicionais

<table><thead><tr><th width="192">Campo</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Anexos</strong></td><td>Upload de arquivos relacionados à configuração do benefício (regulamentos, portarias, manuais). Aceita múltiplos arquivos.</td></tr><tr><td><strong>Observações</strong></td><td>Texto livre para notas internas sobre a configuração.</td></tr></tbody></table>

### O que acontece ao salvar

Ao clicar em **Criar**, o sistema:

1. Salva a configuração do benefício
2. **Gera automaticamente** todas as permissões dinâmicas para este benefício (\~28 permissões com o padrão `BENEFICIO_{ID}_*` e `BENEFICIARIOS_{ID}_*`)
3. Atribui todas as permissões geradas ao perfil **Administrador** automaticamente

A partir deste ponto, os próximos passos são: vincular equipamentos/organizações, atribuir permissões a perfis de técnicos, e publicar o benefício.

***

## Configurar Acompanhamento

Esta página detalha como funciona o sistema de acompanhamento periódico dos beneficiários. A configuração é feita na criação/edição do benefício (campos já descritos acima), mas aqui exploramos o funcionamento em mais profundidade.

### Quando usar acompanhamento

Habilite o acompanhamento quando o benefício exigir registros periódicos sobre a situação dos beneficiários. Exemplos:

* Relatório mensal de frequência de participantes
* Avaliação bimestral de metas
* Registro trimestral de atividades realizadas
* Prestação de contas semestral

Se o benefício é uma concessão pontual (ex: entrega única de kit, aprovação de cadastro sem acompanhamento), deixe desabilitado.

### Preparação do formulário de acompanhamento

Antes de configurar o acompanhamento no benefício:

1. Acesse o módulo de **Formulários**
2. Crie um formulário com os campos que serão preenchidos a cada período (ex: "Frequência no mês", "Observações do técnico", "Situação atual")
3. Publique a versão do formulário

Este formulário pode ser completamente diferente do formulário de cadastro — cada um tem seu propósito.

### Como a periodicidade define as referências

A periodicidade escolhida determina automaticamente as opções de referência disponíveis ao registrar um acompanhamento:

<table><thead><tr><th width="149.3333740234375">Periodicidade</th><th>Opções de referência</th></tr></thead><tbody><tr><td><strong>Mensal</strong></td><td>Janeiro, Fevereiro, Março, Abril, Maio, Junho, Julho, Agosto, Setembro, Outubro, Novembro, Dezembro</td></tr><tr><td><strong>Bimestral</strong></td><td>1º Bimestre, 2º Bimestre, 3º Bimestre, 4º Bimestre, 5º Bimestre, 6º Bimestre</td></tr><tr><td><strong>Trimestral</strong></td><td>1º Trimestre, 2º Trimestre, 3º Trimestre, 4º Trimestre</td></tr><tr><td><strong>Semestral</strong></td><td>1º Semestre, 2º Semestre</td></tr><tr><td><strong>Anual</strong></td><td>Anual</td></tr></tbody></table>

### Regra de duplicidade

O sistema impede que um mesmo beneficiário tenha dois acompanhamentos para o mesmo **ano + referência**. Ao registrar, os períodos já preenchidos aparecem desabilitados no seletor.

### Status ativo e pendências

O campo **"Status Ativo"** da configuração define quais beneficiários são considerados ativos para fins de cobrança de pendências. Apenas beneficiários cujo cadastro possua um dos status marcados como ativos aparecerão na lista de pendentes no painel gerencial de acompanhamento.

Exemplo: se o benefício possui status "Ativo", "Em Acompanhamento", "Desligado" e "Suspenso", e os status ativos configurados são "Ativo" e "Em Acompanhamento", apenas beneficiários nesses dois status gerarão pendência quando o período não for preenchido.

***

## Configurar Equipamentos e Organizações

Após criar o benefício, é necessário definir quais equipamentos (e opcionalmente organizações) podem operá-lo. Essa configuração é acessada pela sidebar do benefício nas opções **"Configurar equipamentos"** e **"Configurar organizações"**.

### Por que vincular equipamentos?

O vínculo de equipamentos é o mecanismo central de controle de acesso operacional no SIAD Benefícios. Ele garante que:

* O técnico do CRCM ABC só veja beneficiários cadastrados pelo CRCM ABC
* O técnico do CRCM XYZ não consiga cadastrar beneficiários em nome do CRCM ABC
* Cada equipamento tenha autonomia sobre seus próprios cadastros

Sem o vínculo configurado, o benefício não aparecerá para nenhum técnico (exceto aqueles com permissão `ACESSAR_GLOBAL`).

### Como vincular equipamentos

1. Acesse **Benefícios > Configurações** e selecione o benefício
2. Na sidebar, clique em **"Configurar equipamentos"**
3. Adicione os equipamentos que poderão operar este benefício
4. Salve

A partir desse momento, técnicos lotados nesses equipamentos (e que possuam a permissão `BENEFICIARIOS_{ID}_ACESSAR`) poderão ver a aba do benefício na listagem de cadastros.

### Como vincular organizações

O processo é idêntico, mas via **"Configurar organizações"**. Organizações são tipicamente usadas quando o benefício é operado por entidades parceiras (ONGs, associações etc.) em conjunto com os equipamentos públicos.

### Efeito sobre o formulário de cadastro

As configurações de equipamento/organização definidas na criação do benefício afetam diretamente o comportamento do formulário:

<table><thead><tr><th width="245.3333740234375">Configuração</th><th>Efeito no formulário</th></tr></thead><tbody><tr><td>Equipamento habilitado</td><td>Campo "Equipamento de vínculo" aparece no formulário de cadastro, listando apenas equipamentos vinculados ao benefício</td></tr><tr><td>Obrigatório</td><td>O campo não pode ficar vazio</td></tr><tr><td>Exibir logado por padrão</td><td>O campo vem pré-preenchido com o equipamento do técnico</td></tr><tr><td>Bloquear edição</td><td>O técnico não consegue alterar (fica travado no seu equipamento)</td></tr></tbody></table>

Para usuários com permissão `CADASTRAR_GLOBAL`, o bloqueio é ignorado — eles podem cadastrar beneficiários em qualquer equipamento vinculado.

### Escopo de visibilidade — resumo

| Tipo de usuário                        | O que vê na listagem                          |
| -------------------------------------- | --------------------------------------------- |
| Técnico com permissão `ACESSAR`        | Apenas cadastros do seu próprio equipamento   |
| Técnico com permissão `ACESSAR_GLOBAL` | Cadastros de todos os equipamentos vinculados |
| Administrador do Sistema               | Todos os cadastros                            |

***

## Configurar Permissões

O SIAD Benefícios utiliza um sistema de permissões dinâmicas — cada benefício gera automaticamente seu próprio conjunto de permissões ao ser criado. Esta página explica como visualizar, entender e atribuir essas permissões.

### Acessar a tela de permissões

1. Acesse **Benefícios > Configurações** e selecione o benefício
2. Na sidebar, clique em **"Configurar permissões"**

A tela exibe todas as permissões geradas para aquele benefício, agrupadas por categoria, com indicação de quais perfis possuem cada uma.

### Permissões geradas automaticamente

Ao criar um benefício de ID `5`, o sistema gera o seguinte conjunto:

#### Permissões de configuração (gestor)

<table><thead><tr><th width="309.3333740234375">Permissão</th><th>Descrição</th></tr></thead><tbody><tr><td><code>BENEFICIO_5_CONSULTAR</code></td><td>Visualizar as configurações do benefício</td></tr><tr><td><code>BENEFICIO_5_ALTERAR</code></td><td>Editar configurações, formulários e vínculos</td></tr><tr><td><code>BENEFICIO_5_EXCLUIR</code></td><td>Excluir o benefício</td></tr><tr><td><code>BENEFICIO_5_REATIVAR</code></td><td>Restaurar benefício excluído</td></tr><tr><td><code>BENEFICIO_5_CONFIGURACOES_GERAIS</code></td><td>Acessar configurações gerais avançadas</td></tr></tbody></table>

#### Permissões operacionais de cadastro (técnico)

<table><thead><tr><th width="263.333251953125">Permissão</th><th>Descrição</th></tr></thead><tbody><tr><td><code>BENEFICIARIOS_5_ACESSAR</code></td><td>Ver a aba deste benefício na listagem. Essencial — sem ela o benefício fica invisível para o técnico.</td></tr><tr><td><code>BENEFICIARIOS_5_CADASTRAR</code></td><td>Inserir um novo beneficiário</td></tr><tr><td><code>BENEFICIARIOS_5_CONSULTAR</code></td><td>Visualizar dados de cadastros existentes</td></tr><tr><td><code>BENEFICIARIOS_5_ALTERAR</code></td><td>Editar formulário e status dos cadastros</td></tr><tr><td><code>BENEFICIARIOS_5_EXCLUIR</code></td><td>Excluir cadastros (soft delete)</td></tr><tr><td><code>BENEFICIARIOS_5_REATIVAR</code></td><td>Restaurar cadastros excluídos</td></tr></tbody></table>

#### Permissões de acesso expandido (supervisor)

<table><thead><tr><th width="307.333251953125">Permissão</th><th>Descrição</th></tr></thead><tbody><tr><td><code>BENEFICIARIOS_5_ACESSAR_GLOBAL</code></td><td>Ignora a restrição de equipamento — vê cadastros de todos os equipamentos</td></tr><tr><td><code>BENEFICIARIOS_5_CADASTRAR_GLOBAL</code></td><td>Permite cadastrar beneficiários em qualquer equipamento (desbloqueia o campo de equipamento)</td></tr></tbody></table>

#### Permissões de acompanhamento

| Permissão                                         | Descrição                                                            |
| ------------------------------------------------- | -------------------------------------------------------------------- |
| `BENEFICIARIOS_5_ACOMPANHAMENTO_ACESSAR`          | Ver a aba/botão de acompanhamento                                    |
| `BENEFICIARIOS_5_ACOMPANHAMENTO_CADASTRAR`        | Registrar acompanhamentos (restrito ao seu equipamento)              |
| `BENEFICIARIOS_5_ACOMPANHAMENTO_CADASTRAR_GLOBAL` | Registrar acompanhamentos para beneficiários de qualquer equipamento |
| `BENEFICIARIOS_5_ACOMPANHAMENTO_CONSULTAR`        | Visualizar acompanhamentos registrados                               |
| `BENEFICIARIOS_5_ACOMPANHAMENTO_ALTERAR`          | Editar acompanhamentos existentes                                    |
| `BENEFICIARIOS_5_ACOMPANHAMENTO_EXCLUIR`          | Excluir acompanhamentos                                              |

#### Permissões administrativas

<table><thead><tr><th width="496">Permissão</th><th>Descrição</th></tr></thead><tbody><tr><td><code>BENEFICIARIOS_5_EQUIPAMENTOS_ACESSAR</code></td><td>Ver a tela de configuração de equipamentos</td></tr><tr><td><code>BENEFICIARIOS_5_EQUIPAMENTOS_CADASTRAR</code></td><td>Vincular novos equipamentos</td></tr><tr><td><code>BENEFICIARIOS_5_EQUIPAMENTOS_EXCLUIR</code></td><td>Desvincular equipamentos</td></tr><tr><td><code>BENEFICIARIOS_5_ORGANIZACOES_ACESSAR/CADASTRAR/EXCLUIR</code></td><td>Idem para organizações</td></tr><tr><td><code>BENEFICIARIOS_5_PERMISSOES_ACESSAR/CADASTRAR/EXCLUIR</code></td><td>Gerenciar a tela de permissões</td></tr></tbody></table>

### Como atribuir permissões a perfis

1. Acesse o painel de **Administração > Perfis**
2. Crie um novo perfil (ex: "Técnico Auxílio Aluguel") ou edite um existente
3. Na busca de permissões, procure pelo ID do benefício (ex: pesquisar por "5" ou "BENEFICIARIOS\_5")
4. Selecione as permissões necessárias para o perfil
5. Associe o perfil aos usuários que atuarão no benefício

#### Exemplo: perfil típico de técnico

Para um técnico que opera o dia-a-dia de cadastros:

* `BENEFICIARIOS_5_ACESSAR` ✓
* `BENEFICIARIOS_5_CADASTRAR` ✓
* `BENEFICIARIOS_5_CONSULTAR` ✓
* `BENEFICIARIOS_5_ALTERAR` ✓
* `BENEFICIARIOS_5_ACOMPANHAMENTO_ACESSAR` ✓
* `BENEFICIARIOS_5_ACOMPANHAMENTO_CADASTRAR` ✓
* `BENEFICIARIOS_5_ACOMPANHAMENTO_CONSULTAR` ✓

#### Exemplo: perfil de coordenador/supervisor

Para quem precisa ver a rede toda:

* Todas as permissões do técnico +
* `BENEFICIARIOS_5_ACESSAR_GLOBAL` ✓
* `BENEFICIARIOS_5_CADASTRAR_GLOBAL` ✓
* `BENEFICIARIOS_5_ACOMPANHAMENTO_CADASTRAR_GLOBAL` ✓
* `BENEFICIARIOS_5_EXCLUIR` ✓
* `BENEFICIARIOS_5_REATIVAR` ✓

### Gerar permissões faltantes

Com o tempo, atualizações do sistema podem introduzir novas permissões que benefícios antigos ainda não possuem. Para sincronizar:

1. Acesse a tela **"Configurar permissões"** do benefício
2. Clique no botão **"Gerar Permissões Faltantes"**
3. O sistema varrerá as permissões esperadas pelo código e criará as que ainda não existem no banco

Isso não afeta permissões já existentes nem remove atribuições de perfis.

> **Nota técnica**: esse processo também é executado automaticamente nos deploys via o comando `php artisan beneficios:gerar-permissoes-faltantes`.

***

## Publicar o Benefício

Após configurar formulários, equipamentos, organizações e permissões, o último passo é publicar o benefício para torná-lo operacional.

### Checklist pré-publicação

Antes de alterar o status para Publicado, confirme:

* [ ] **Formulário de cadastro** criado e com versão publicada
* [ ] **Formulário de acompanhamento** criado e com versão publicada (se aplicável)
* [ ] **Status permitidos** cadastrados (pelo menos um)
* [ ] **Equipamentos vinculados** ao benefício (pelo menos um, se habilitado)
* [ ] **Organizações vinculadas** (se habilitado)
* [ ] **Permissões atribuídas** a pelo menos um perfil de técnico
* [ ] **Perfil atribuído** aos usuários que operarão o benefício

### Como publicar

1. Acesse **Benefícios > Configurações** e selecione o benefício
2. Clique em **Editar** (na sidebar ou no botão de ação)
3. Altere o campo **Status** de "Rascunho" para **"Publicado"**
4. Salve

### Verificação pós-publicação

Após publicar, valide o acesso com um usuário técnico:

1. Acesse o sistema com um usuário que possua as permissões configuradas
2. Verifique se a **aba do benefício** aparece na listagem de cadastros (menu Benefícios > Beneficiários)
3. Clique em **"Cadastrar Beneficiário"** e confirme que o formulário é renderizado corretamente
4. Cadastre um beneficiário de teste e verifique se o status é salvo
5. Se o acompanhamento estiver habilitado, acesse o cadastro e registre um acompanhamento de teste
6. Verifique o **painel de acompanhamento** (menu Benefícios > Acompanhamento) para confirmar que pendências são geradas corretamente

### Despublicar ou arquivar

Se for necessário suspender o benefício:

* **Alterar para Rascunho**: remove o benefício da listagem dos técnicos. Cadastros existentes permanecem no banco mas ficam inacessíveis para operação.
* **Alterar para Arquivado**: desativa permanentemente. Dados existentes permanecem consultáveis para Administradores do Sistema.

Em ambos os casos, os dados já cadastrados (beneficiários e acompanhamentos) não são excluídos.
