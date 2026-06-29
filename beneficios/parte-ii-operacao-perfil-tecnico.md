# Parte II — Operação (perfil técnico)

## Cadastrar um Beneficiário

Para cadastrar uma pessoa em um benefício, acesse o menu lateral **Benefícios > Beneficiários** e clique em **"Cadastrar Beneficiário"**.

Alternativamente, é possível iniciar o cadastro diretamente a partir do perfil da pessoa (no módulo de Atendimento), onde o campo "Pessoa" já virá pré-preenchido.

### Navegação por abas

A listagem de beneficiários é organizada em **abas**, onde cada aba representa um benefício publicado ao qual o técnico tem acesso. A aba visível depende de:

1. O técnico possuir a permissão `BENEFICIARIOS_{ID}_ACESSAR` (ou `ACESSAR_GLOBAL`)
2. O equipamento do técnico estar vinculado ao benefício (exceto se tiver acesso global)

O botão **"Cadastrar Beneficiário"** já envia o ID da aba ativa como parâmetro, pré-selecionando o benefício no formulário de cadastro.

### Formulário de cadastro

O formulário é composto por uma seção fixa (Benefício) e seções dinâmicas que variam conforme o formulário vinculado.

#### Seção fixa — Benefício

<table><thead><tr><th width="205">Campo</th><th width="135" align="center">Obrigatório</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Benefício</strong></td><td align="center">Sim</td><td>Seleção do benefício. Lista apenas benefícios publicados cujo equipamento do usuário está vinculado (ou todos, se tiver permissão global).</td></tr><tr><td><strong>Pessoa</strong></td><td align="center">Sim</td><td>Busca de pessoa cadastrada no SIAD. Permite pesquisar por nome, CPF ou NIS. Se o cadastro for iniciado a partir do perfil da pessoa, já vem preenchido.</td></tr><tr><td><strong>Equipamento de vínculo</strong></td><td align="center">Condicional</td><td>Selecione o equipamento responsável pelo cadastro. Comportamento varia conforme configuração do benefício (pode vir pré-preenchido e/ou bloqueado). Lista apenas equipamentos vinculados ao benefício.</td></tr><tr><td><strong>Organização de vínculo</strong></td><td align="center">Condicional</td><td>Selecione a organização parceira. Visível apenas quando "Habilitar Organização" está ativo na configuração do benefício. Lista apenas organizações vinculadas.</td></tr><tr><td><strong>Status</strong></td><td align="center">Sim</td><td>Selecione o status inicial do cadastro entre os status permitidos configurados no benefício (ex: "Em Análise", "Ativo").</td></tr></tbody></table>

#### Seções dinâmicas — Formulário

Após selecionar o benefício e a pessoa, o sistema renderiza automaticamente as seções e campos do formulário de cadastro vinculado ao benefício. Todos os tipos de atributo do SIAD Forms estão disponíveis (Texto, Lista, CEP, Data, Repeater etc.).

Os campos dinâmicos funcionam exatamente como nos formulários do SIAD Forms, incluindo:

* Campos condicionais (dependência de campo pai)
* Validações (obrigatoriedade, tamanho, regex)
* Seções condicionais (visíveis apenas quando um campo pai tem determinado valor)

### Regra de duplicidade

O sistema não permite cadastrar a mesma pessoa duas vezes no mesmo benefício. Ao tentar, a validação exibirá a mensagem: _"Esta pessoa já está cadastrada neste benefício."_

### Comportamento do campo Equipamento

O campo de equipamento segue regras baseadas na configuração do benefício:

| Configuração                    | Comportamento para técnico comum      | Comportamento para quem tem `CADASTRAR_GLOBAL`       |
| ------------------------------- | ------------------------------------- | ---------------------------------------------------- |
| Exibir logado + Bloquear edição | Travado no equipamento do técnico     | Livre para selecionar qualquer equipamento vinculado |
| Exibir logado (sem bloqueio)    | Pré-preenchido, mas editável          | Livre                                                |
| Sem exibir logado               | Vazio, seleção livre entre vinculados | Livre                                                |

***

## Consultar e Editar Cadastros

A listagem de cadastros é a tela principal de operação dos técnicos. Acesse via **Benefícios > Beneficiários** e selecione a aba do benefício desejado.

### Colunas da listagem

<table><thead><tr><th width="234.6666259765625">Coluna</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Cód. Benefício (SIAD)</strong></td><td>Código único gerado automaticamente (últimos 10 caracteres do UUID). Copiável.</td></tr><tr><td><strong>Pessoa Beneficiária</strong></td><td>Nome, CPF e NIS da pessoa vinculada.</td></tr><tr><td><strong>Equipamento</strong></td><td>Equipamento de vínculo do cadastro. Visível apenas para usuários com acesso global.</td></tr><tr><td><strong>Organização</strong></td><td>Organização de vínculo. Visível apenas quando o benefício tem organização habilitada.</td></tr><tr><td><strong>Status</strong></td><td>Status atual do cadastro.</td></tr><tr><td><strong>Colunas dinâmicas</strong></td><td>Todos os atributos do formulário de cadastro aparecem como colunas ocultas por padrão. Podem ser ativadas pelo gerenciador de colunas. Pesquisáveis e ordenáveis.</td></tr><tr><td><strong>Registrado</strong></td><td>Data e usuário de criação.</td></tr><tr><td><strong>Alterado</strong></td><td>Data e usuário da última alteração (oculta por padrão).</td></tr></tbody></table>

### Filtros disponíveis

<table><thead><tr><th width="199.333251953125">Filtro</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Status</strong></td><td>Filtra por status do cadastro (lista os status existentes nos registros).</td></tr><tr><td><strong>Equipamento</strong></td><td>Visível para usuários com acesso global. Filtra por equipamento de vínculo.</td></tr><tr><td><strong>Organização</strong></td><td>Visível quando o benefício tem organização habilitada. Filtra por organização de vínculo.</td></tr><tr><td><strong>Registro excluído</strong></td><td>Permite incluir ou exibir apenas cadastros excluídos.</td></tr></tbody></table>

### Badge de contagem

Cada aba exibe um **badge** com a quantidade de cadastros visíveis para o técnico. Para técnicos comuns, reflete apenas os cadastros do seu equipamento. Para supervisores com acesso global, reflete o total.

### Escopo de visibilidade

<table><thead><tr><th width="274">Perfil</th><th>O que vê</th></tr></thead><tbody><tr><td>Técnico comum</td><td>Cadastros do seu próprio equipamento (ou organização)</td></tr><tr><td>Técnico com <code>ACESSAR_GLOBAL</code></td><td>Cadastros de todos os equipamentos e organizações vinculados</td></tr><tr><td>Administrador do Sistema</td><td>Todos os cadastros</td></tr></tbody></table>

### Visualizar um cadastro

Clique no botão de visualização (ícone de olho) na linha do cadastro. A tela exibe:

* Informações do benefício e da pessoa
* Status atual
* Equipamento e organização de vínculo
* Todos os dados preenchidos no formulário dinâmico (organizados por seção)
* Informações de auditoria (quem cadastrou, quando, última alteração)

A **sidebar** lateral oferece navegação rápida:

<table><thead><tr><th width="265.333251953125">Item</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Visualizar Beneficiário</strong></td><td>Tela de consulta (atual)</td></tr><tr><td><strong>Ir para o Cadastro da Pessoa</strong></td><td>Link direto para o perfil da pessoa no módulo de Atendimento</td></tr><tr><td><strong>Editar Beneficiário</strong></td><td>Formulário de edição</td></tr><tr><td><strong>Acompanhamento</strong></td><td>Listagem de acompanhamentos (com badge de contagem). Visível apenas se o benefício tiver acompanhamento habilitado e o usuário tiver permissão.</td></tr></tbody></table>

### Editar um cadastro

Clique no botão de edição (ícone de lápis) na listagem ou acesse pela sidebar. O formulário de edição exibe os mesmos campos do cadastro, com as seguintes particularidades:

* O campo **Benefício** fica desabilitado (não é possível transferir um cadastro entre benefícios)
* O campo **Pessoa** fica desabilitado (não é possível trocar a pessoa)
* O campo **Status** pode ser alterado (ex: mudar de "Em Análise" para "Ativo")
* Todos os campos dinâmicos do formulário podem ser editados
* O campo de Equipamento respeita as mesmas regras de bloqueio da criação

***

## Registrar Acompanhamento

O acompanhamento permite registrar informações periódicas sobre cada beneficiário. Para acessá-lo, navegue até o cadastro do beneficiário e clique em **"Acompanhamento"** na sidebar lateral.

### Pré-requisitos

* O benefício deve ter a opção **"Habilitar acompanhamento?"** ativa
* O técnico deve possuir a permissão `BENEFICIARIOS_{ID}_ACOMPANHAMENTO_ACESSAR`

### Listagem de acompanhamentos

A tela exibe todos os acompanhamentos já registrados para aquele beneficiário, com as seguintes colunas:

<table><thead><tr><th width="221.3333740234375">Coluna</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Ano</strong></td><td>Ano de referência do acompanhamento.</td></tr><tr><td><strong>Referência</strong></td><td>Período (Janeiro, 1º Bimestre, etc. conforme periodicidade).</td></tr><tr><td><strong>Equipamento</strong></td><td>Equipamento que registrou. Visível para usuários com acesso global.</td></tr><tr><td><strong>Organização</strong></td><td>Organização vinculada. Visível quando habilitada.</td></tr><tr><td><strong>Colunas dinâmicas</strong></td><td>Atributos do formulário de acompanhamento (ocultas por padrão, ativáveis).</td></tr><tr><td><strong>Registrado / Alterado</strong></td><td>Dados de auditoria.</td></tr></tbody></table>

A listagem é ordenada por data de referência (mais recentes primeiro).

### Registrar novo acompanhamento

Clique em **"Registrar Acompanhamento"** no topo da listagem. Um modal será aberto com os seguintes campos:

#### Dados Gerais

<table><thead><tr><th width="186.3333740234375">Campo</th><th width="138.6666259765625" align="center">Obrigatório</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Pessoa</strong></td><td align="center">—</td><td>Exibido como referência (desabilitado). Mostra a pessoa vinculada ao cadastro.</td></tr><tr><td><strong>Equipamento</strong></td><td align="center">Condicional</td><td>Equipamento responsável pelo registro. Mesmo comportamento de bloqueio do cadastro.</td></tr><tr><td><strong>Organização</strong></td><td align="center">Condicional</td><td>Organização responsável. Mesmas regras do cadastro.</td></tr><tr><td><strong>Ano</strong></td><td align="center">Sim</td><td>Selecione o ano de referência. Lista os 2 anos anteriores, o atual e o próximo.</td></tr><tr><td><strong>Referência</strong></td><td align="center">Sim</td><td>Selecione o período. As opções dependem da periodicidade configurada no benefício. <strong>Períodos já preenchidos ficam desabilitados</strong> (não é possível registrar duplicatas).</td></tr></tbody></table>

#### Formulário dinâmico

Abaixo dos dados gerais, o sistema renderiza as seções e campos do formulário de acompanhamento vinculado ao benefício. Funciona como qualquer formulário do SIAD Forms.

### Regra de duplicidade

Não é permitido registrar dois acompanhamentos para o mesmo **ano + referência** de um mesmo cadastro. Se o técnico selecionar um período já preenchido:

* A opção aparece desabilitada no seletor
* Se forçar de outra forma, a validação exibirá: _"Já existe um acompanhamento registrado para este período."_

### Editar acompanhamento

Clique no botão de edição (ícone de lápis) na linha do acompanhamento. O mesmo modal é aberto com os dados preenchidos, permitindo ajustes.

A edição está disponível para:

* Usuários com permissão `BENEFICIARIOS_{ID}_ACOMPANHAMENTO_ALTERAR` (restrito ao seu equipamento)
* Usuários com permissão `BENEFICIARIOS_{ID}_ACOMPANHAMENTO_CADASTRAR_GLOBAL` (qualquer equipamento)

### Excluir acompanhamento

Disponível para usuários com permissão `BENEFICIARIOS_{ID}_ACOMPANHAMENTO_EXCLUIR`. A exclusão é definitiva (não é soft delete neste caso).

### Quem pode registrar acompanhamentos

A permissão de cadastrar acompanhamentos respeita o vínculo de equipamento:

<table><thead><tr><th width="340">Perfil</th><th>Pode registrar para</th></tr></thead><tbody><tr><td>Técnico com <code>ACOMPANHAMENTO_CADASTRAR</code></td><td>Beneficiários do seu equipamento (ou organização)</td></tr><tr><td>Técnico com <code>ACOMPANHAMENTO_CADASTRAR_GLOBAL</code></td><td>Beneficiários de qualquer equipamento</td></tr></tbody></table>

***

## Painel de Acompanhamento (Pendências)

O painel de acompanhamento oferece uma visão gerencial que permite identificar rapidamente quais beneficiários estão com acompanhamento pendente para determinado período. Acesse via **Benefícios > Acompanhamento** no menu lateral.

### Filtros

A tela apresenta três filtros sequenciais no topo:

<table><thead><tr><th width="206.6666259765625">Filtro</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Benefício</strong></td><td>Selecione o benefício que deseja consultar. Lista apenas benefícios publicados, com acompanhamento habilitado e aos quais o técnico tem acesso. Se o técnico tiver acesso a apenas um benefício, ele é pré-selecionado automaticamente.</td></tr><tr><td><strong>Ano</strong></td><td>Selecione o ano de referência. Disponível após selecionar o benefício.</td></tr><tr><td><strong>Período de referência</strong></td><td>Selecione o período (Janeiro, 1º Bimestre etc.). As opções dependem da periodicidade do benefício. Disponível após selecionar o ano.</td></tr></tbody></table>

Os filtros são sequenciais: o campo "Ano" só aparece após selecionar o benefício, e o campo "Período" só aparece após selecionar o ano.

### Resultado da consulta

Após preencher os três filtros, o sistema exibe duas tabelas:

#### Tabela 1 — Acompanhamentos registrados

Lista todos os acompanhamentos já realizados para o período selecionado. Exibe os dados preenchidos no formulário e permite visualização/edição direta.

#### Tabela 2 — Beneficiários pendentes

Lista os beneficiários que **ainda não possuem acompanhamento** registrado para o período selecionado. Apenas beneficiários com status considerado "ativo" (conforme configuração do benefício) aparecem nesta tabela.

Esta visão permite ao coordenador:

* Identificar quais beneficiários estão sem acompanhamento no mês/bimestre
* Cobrar ou redistribuir os registros pendentes
* Registrar acompanhamentos diretamente a partir desta tela (botão de ação na linha do beneficiário pendente)

### Quem pode acessar o painel

O painel é visível para usuários com a permissão geral `BENEFICIARIOS_ACOMPANHAMENTO_ACESSAR`. O conteúdo exibido respeita as mesmas regras de escopo:

* Técnicos comuns veem apenas beneficiários do seu equipamento
* Técnicos com acesso global veem toda a rede
* A listagem de benefícios no filtro respeita vínculo de equipamento + permissão `ACESSAR`

### Utilidade prática

O painel é especialmente útil para:

* Coordenadores que precisam acompanhar a regularidade dos registros da equipe
* Gestores que precisam gerar relatórios de cobertura por período
* Técnicos que querem verificar quais beneficiários do seu equipamento ainda precisam de registro no mês

> **Dica**: para análises mais detalhadas, exportação de dados e criação de indicadores sobre cobertura de acompanhamento, utilize o **Metabase**, que está conectado à base de dados do SIAD e permite consultas personalizadas sobre as tabelas de acompanhamentos e cadastros.
