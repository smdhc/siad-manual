# Parte I — Configurações (perfil administrador)

## Configurações do Acompanhamento Mensal

As configurações do acompanhamento mensal definem as janelas de tempo em que os equipamentos podem registrar e editar frequências, além dos valores financeiros do benefício. Acesse via **Transcidadania > Configurações** (visível apenas para usuários com permissão `TRANSCIDADANIA_ADMINISTRAR`).

### Janelas de preenchimento

O registro de frequências funciona com um sistema de **duas janelas** temporais. Fora dessas janelas, apenas administradores podem registrar ou editar frequências.

#### 1ª Janela — Prazo principal

Abre no **primeiro dia do mês seguinte** ao mês de referência e permanece aberta por um número configurável de dias.

Exemplo com configuração padrão (12 dias): a frequência de março pode ser registrada entre 1º e 12 de abril.

#### 2ª Janela — Janela de correções

Uma segunda janela de edição é aberta após o fim da primeira, em uma data configurável, com duração também configurável.

Exemplo com configuração padrão (início aos 23 dias, duração de 7 dias): a segunda janela para a frequência de março abre em 24 de abril e fecha em 30 de abril.

#### Campos de configuração

<table><thead><tr><th width="248.666748046875">Campo</th><th width="375">Descrição</th><th>Padrão</th></tr></thead><tbody><tr><td><strong>Prazo para preenchimento (dias)</strong></td><td>Duração da 1ª janela a partir do início do mês seguinte ao mês de referência.</td><td>12 dias</td></tr><tr><td><strong>Prazo em dias para início da segunda janela de correções</strong></td><td>Quantos dias após o início do mês seguinte a 2ª janela abre.</td><td>23 dias</td></tr><tr><td><strong>Duração em dias da segunda janela de correções</strong></td><td>Por quantos dias a 2ª janela permanece aberta.</td><td>7 dias</td></tr></tbody></table>

#### Comportamento para diferentes perfis

| Perfil                                   | Comportamento                                                        |
| ---------------------------------------- | -------------------------------------------------------------------- |
| Técnico comum                            | Só pode registrar/editar dentro das janelas configuradas             |
| Usuário com `TRANSCIDADANIA_ADMINISTRAR` | Pode registrar/editar frequências de qualquer mês a qualquer momento |

#### Restrições adicionais na seleção de mês

Ao registrar uma frequência, o sistema aplica as seguintes restrições:

* Meses futuros não podem ser selecionados
* Meses já registrados para a mesma pessoa ficam desabilitados
* Meses fora das janelas ficam desabilitados (para não-administradores)
* Na edição, o mês original permanece habilitado mesmo fora das janelas

### Intervalo de frequência inconsistente

<table><thead><tr><th width="186">Campo</th><th width="417">Descrição</th><th>Padrão</th></tr></thead><tbody><tr><td><strong>Período em meses para identificar inconsistência</strong></td><td>Define o intervalo retroativo (em meses) considerado para contabilizar os meses com frequência "NÃO PAGAR" ou "POSSIBILIDADE DE DESLIGAMENTO". Se o beneficiário acumular 3 ou mais meses nessa condição dentro do intervalo, o sistema gera alerta de inconsistência.</td><td>12 meses</td></tr></tbody></table>

### Pagamentos

#### Habilitar pagamento

<table><thead><tr><th width="214.6666259765625">Campo</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Habilitar pagamento</strong></td><td>Toggle que controla se o campo de valor de pagamento é exibido no formulário de frequência. Quando desabilitado, os campos de valor não aparecem (mas o cálculo de desconto continua sendo gravado internamente).</td></tr></tbody></table>

#### Histórico de valores anuais do benefício

O valor mensal do benefício pode variar de ano para ano. A configuração permite registrar o valor vigente por ano:

<table><thead><tr><th width="151.3333740234375">Campo</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Ano</strong></td><td>Ano de vigência do valor. Não permite duplicatas.</td></tr><tr><td><strong>Valor</strong></td><td>Valor em reais (R$) do benefício mensal para aquele ano.</td></tr></tbody></table>

Ao adicionar ou alterar um valor, clique em **"Adicionar"** para incluir um novo ano. Ao salvar as configurações:

* O sistema atualiza automaticamente **todas as frequências** do ano correspondente com o novo valor
* O recálculo aplica o desconto já gravado ao novo valor base
* Esse processo pode levar alguns minutos em anos com muitas frequências

> **Atenção**: em caso de alterações nos valores, o processo de gravação poderá levar alguns minutos, pois todas as frequências do ano correspondente serão atualizadas.

***

## Configurações do PIA

O PIA (Plano Individual de Atendimento) é composto por múltiplos formulários dinâmicos que documentam o planejamento e a evolução de cada pessoa beneficiária. A configuração define quais formulários compõem o PIA e o prazo para sinalizar necessidade de atualização.

### Prazo de atualização

<table><thead><tr><th>Campo</th><th width="461.666748046875">Descrição</th><th>Padrão</th></tr></thead><tbody><tr><td><strong>Prazo de atualização (dias)</strong></td><td>Define após quantos dias sem atualização o registro PIA será sinalizado como "Atualização pendente". Quando o registro ultrapassa esse prazo desde a última edição, o status na tabela PIA muda automaticamente para "Atualização pendente" (badge amarelo).</td><td>90 dias</td></tr></tbody></table>

### Formulários PIA

O PIA pode conter múltiplos formulários, cada um voltado a uma dimensão de acompanhamento (ex: "Dados Socioeconômicos", "Saúde", "Educação", "Metas Profissionais").

#### Campos de configuração por formulário

<table><thead><tr><th width="159">Campo</th><th width="130" align="center">Obrigatório</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Título</strong></td><td align="center">Sim</td><td>Nome do formulário PIA exibido na tabela para o técnico. Ex: "Saúde e Bem-Estar", "Projeto Profissional".</td></tr><tr><td><strong>Formulário</strong></td><td align="center">Sim</td><td>Selecione o formulário dinâmico do SIAD que será utilizado. Somente formulários com versão publicada são listados.</td></tr><tr><td><strong>Versão</strong></td><td align="center">Sim</td><td>Selecione a versão publicada do formulário.</td></tr><tr><td><strong>Ordem</strong></td><td align="center">Sim</td><td>Posição numérica na lista de formulários PIA. Menor = mais acima.</td></tr></tbody></table>

#### Como gerenciar

* Clique em **"Adicionar formulário"** para incluir um novo formulário ao PIA
* Cada linha pode ser editada ou removida
* A remoção soft-deleta a configuração — registros já preenchidos permanecem consultáveis
* Ao alterar a versão de um formulário já em uso, registros preenchidos em versão anterior são sinalizados como "Preenchido (versão desatualizada)"

#### Pré-requisito

Os formulários utilizados no PIA são os mesmos formulários dinâmicos do SIAD (criados em **Formulários > Formulários**). Antes de configurá-los aqui, é necessário:

1. Criar o formulário no módulo de [Formulários](../forms/introducao.md)
2. Configurar as seções e atributos desejados
3. Publicar a versão do formulário

***

## Permissões e Acesso

O módulo Transcidadania utiliza um conjunto fixo de permissões (diferente do SIAD Benefícios, onde são dinâmicas por ID). Todas as permissões começam com o prefixo `TRANSCIDADANIA_`.

### Requisitos para acesso

Para que o módulo seja visível para um usuário, **duas condições** devem ser atendidas:

1. O usuário deve possuir a permissão `TRANSCIDADANIA_ACESSAR`
2. O equipamento do usuário deve ter o módulo **Transcidadania habilitado** nas configurações do equipamento

Se qualquer uma das condições não for atendida, os menus e abas do Transcidadania ficam invisíveis.

### Como habilitar o módulo no equipamento

1. Acesse **Cadastros > Equipamentos**
2. Edite o equipamento desejado
3. Na seção de módulos habilitados, marque **"Transcidadania"**
4. Salve

A partir desse momento, usuários daquele equipamento (com permissão adequada) passarão a ver o módulo.

### Permissões de cadastro

<table><thead><tr><th width="271.3333740234375">Permissão</th><th>Descrição</th></tr></thead><tbody><tr><td><code>TRANSCIDADANIA_ACESSAR</code></td><td>Ver os menus do módulo e a aba Transcidadania no perfil da pessoa. <strong>Pré-requisito</strong> para todas as demais.</td></tr><tr><td><code>TRANSCIDADANIA_CONSULTAR</code></td><td>Visualizar dados dos cadastros existentes.</td></tr><tr><td><code>TRANSCIDADANIA_CADASTRAR</code></td><td>Inserir novas pessoas no programa.</td></tr><tr><td><code>TRANSCIDADANIA_ALTERAR</code></td><td>Editar cadastros existentes (status, escola, dados do programa).</td></tr><tr><td><code>TRANSCIDADANIA_EXCLUIR</code></td><td>Excluir cadastros (soft delete). Só é possível excluir cadastros que não possuem frequências registradas.</td></tr><tr><td><code>TRANSCIDADANIA_REATIVAR</code></td><td>Restaurar cadastros excluídos.</td></tr></tbody></table>

### Permissões do PIA

<table><thead><tr><th width="296">Permissão</th><th>Descrição</th></tr></thead><tbody><tr><td><code>TRANSCIDADANIA_PIA_CONSULTAR</code></td><td>Visualizar registros PIA preenchidos.</td></tr><tr><td><code>TRANSCIDADANIA_PIA_CADASTRAR</code></td><td>Preencher novos formulários PIA.</td></tr><tr><td><code>TRANSCIDADANIA_PIA_ALTERAR</code></td><td>Editar formulários PIA já preenchidos.</td></tr><tr><td><code>TRANSCIDADANIA_PIA_EXCLUIR</code></td><td>Excluir registros PIA.</td></tr></tbody></table>

### Permissão administrativa

<table><thead><tr><th width="292.6666259765625">Permissão</th><th>Descrição</th></tr></thead><tbody><tr><td><code>TRANSCIDADANIA_ADMINISTRAR</code></td><td>Acesso total: configurações do módulo, bypass de janelas de preenchimento (pode registrar/editar frequências a qualquer momento), exclusão irrestrita.</td></tr></tbody></table>

### Restrições de equipamento

Além das permissões, o sistema aplica restrições por equipamento:

* O técnico só pode editar/excluir frequências registradas pelo **próprio equipamento**
* O cadastro no programa vincula a pessoa ao equipamento do técnico que fez a inserção
* A listagem de cadastros filtra por padrão pelo equipamento do usuário logado (com opção de filtrar por outros equipamentos que tenham o módulo habilitado)
* No painel de acompanhamento (pendentes), são exibidos apenas beneficiários do equipamento do técnico

### Perfis sugeridos

#### Técnico de equipamento

```
TRANSCIDADANIA_ACESSAR
TRANSCIDADANIA_CONSULTAR
TRANSCIDADANIA_CADASTRAR
TRANSCIDADANIA_ALTERAR
TRANSCIDADANIA_PIA_CONSULTAR
TRANSCIDADANIA_PIA_CADASTRAR
TRANSCIDADANIA_PIA_ALTERAR
```

#### Coordenador

Todas as do técnico, mais:

```
TRANSCIDADANIA_EXCLUIR
TRANSCIDADANIA_REATIVAR
TRANSCIDADANIA_PIA_EXCLUIR
```

#### Administrador do programa

```
TRANSCIDADANIA_ADMINISTRAR
```

(Concede acesso irrestrito a todas as funcionalidades, incluindo configurações, bypass de janelas de preenchimento e operações sobre frequências de qualquer equipamento.)
