# Manual

## Configurações

As configurações do Programa de Geração de Renda são acessadas via **Programa de Geração de Renda > Configurações** no menu lateral. Esta página é visível apenas para usuários com a permissão `GERACAO_RENDA_ADMINISTRAR`.

### Configurações gerais

<table><thead><tr><th width="203.3333740234375">Campo</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Exibir callout de dados socioeconômicos</strong></td><td>Quando habilitado, exibe um alerta informativo na aba "Dados Socioeconômicos" do Cadastro da Pessoa, orientando sobre o novo menu de acesso à funcionalidade.</td></tr></tbody></table>

***

### Formulários PIA

O PIA (Plano Individual de Atendimento) é composto por múltiplos formulários dinâmicos que documentam diferentes dimensões do acompanhamento da pessoa no programa. A configuração define quais formulários estão disponíveis.

#### Como adicionar um formulário ao PIA

Clique em **"Adicionar formulário"** na tabela de Formulários PIA. Cada linha representa um formulário e possui os seguintes campos:

<table><thead><tr><th width="129.666748046875">Campo</th><th width="122.3333740234375" align="center">Obrigatório</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Título</strong></td><td align="center">Sim</td><td>Nome do formulário PIA exibido na tabela para o técnico. Ex: "Dados Socioeconômicos", "Projeto Profissional", "Plano de Metas".</td></tr><tr><td><strong>Formulário</strong></td><td align="center">Sim</td><td>Selecione o formulário dinâmico do SIAD que será utilizado. Somente formulários com versão publicada são listados.</td></tr><tr><td><strong>Versão</strong></td><td align="center">Sim</td><td>Selecione a versão publicada do formulário.</td></tr><tr><td><strong>Ordem</strong></td><td align="center">Sim</td><td>Posição numérica na lista de formulários PIA. Menor = mais acima na tabela.</td></tr></tbody></table>

#### Pré-requisito

Os formulários utilizados no PIA são os mesmos formulários dinâmicos do SIAD (criados em **Formulários > Formulários**). Antes de configurá-los aqui, é necessário:

1. Criar o formulário no módulo de Formulários
2. Configurar as seções e atributos desejados
3. Publicar a versão do formulário

#### Gerenciamento

* Formulários podem ser adicionados, editados ou removidos a qualquer momento
* A remoção soft-deleta a configuração — registros já preenchidos permanecem consultáveis
* Ao alterar a versão de um formulário já em uso, registros preenchidos em versão anterior são sinalizados como "Preenchido (versão desatualizada)" na tabela PIA da pessoa
* A ordem pode ser ajustada livremente e afeta apenas a exibição na tabela

#### Salvar

Após realizar todas as alterações desejadas (callout + formulários PIA), clique no botão **"Salvar configurações"** no rodapé da página.

***

## Permissões e Acesso

O módulo de Geração de Renda utiliza um modelo de controle de acesso simplificado baseado no módulo habilitado no equipamento.

### Requisito de acesso

Para que o módulo seja visível, o **equipamento** do usuário deve ter o módulo **"Programa de Geração de Renda"** habilitado nas configurações do equipamento.

#### Como habilitar o módulo no equipamento

1. Acesse **Cadastros > Equipamentos**
2. Edite o equipamento desejado
3. Na seção de módulos habilitados, marque **"Programa de Geração de Renda"**
4. Salve

A partir desse momento, todos os usuários vinculados ao equipamento passarão a visualizar o módulo.

### Permissões disponíveis

<table><thead><tr><th width="246.6666259765625">Permissão</th><th>Descrição</th></tr></thead><tbody><tr><td><code>GERACAO_RENDA_ADMINISTRAR</code></td><td>Acesso administrativo completo: ver cadastros de <strong>todos</strong> os equipamentos (não apenas o próprio), acessar a tela de Configurações, e gerenciar o campo de equipamento durante o cadastro.</td></tr><tr><td><code>GERACAO_RENDA_PIA_EXCLUIR</code></td><td>Permite excluir registros PIA preenchidos. Sem esta permissão, o técnico pode preencher e editar, mas não excluir.</td></tr></tbody></table>

### Controle por equipamento

<table><thead><tr><th width="270.6666259765625">Perfil</th><th>O que vê e pode fazer</th></tr></thead><tbody><tr><td><strong>Técnico</strong> (módulo habilitado, sem permissão admin)</td><td>Vê apenas cadastros do seu equipamento. Pode cadastrar (equipamento travado no seu), editar, preencher/editar PIA.</td></tr><tr><td><strong>Administrador</strong> (com <code>GERACAO_RENDA_ADMINISTRAR</code>)</td><td>Vê cadastros de todos os equipamentos. Pode cadastrar em qualquer equipamento. Acessa Configurações.</td></tr></tbody></table>

### Controle do PIA

<table><thead><tr><th width="274">Ação</th><th>Quem pode</th></tr></thead><tbody><tr><td>Visualizar formulários PIA</td><td>Qualquer usuário com módulo habilitado</td></tr><tr><td>Preencher/editar formulários PIA</td><td>Usuário do mesmo equipamento do cadastro OU administrador</td></tr><tr><td>Excluir registros PIA</td><td>Usuário com permissão <code>GERACAO_RENDA_PIA_EXCLUIR</code></td></tr></tbody></table>

***

## Cadastrar Pessoa no Programa

Para cadastrar uma pessoa no Programa de Geração de Renda, existem dois caminhos:

1. **Pela listagem centralizada**: acesse **Programa de Geração de Renda > Cadastro** e clique em **"Cadastrar Pessoa"**
2. **Pelo perfil da pessoa**: na aba **"Programa de Geração de Renda"** do perfil da pessoa, clique em **"Cadastrar Pessoa"**

O botão de cadastro só aparece se a pessoa ainda não estiver cadastrada no programa.

### Formulário de cadastro

<table><thead><tr><th width="203">Campo</th><th width="133.3333740234375" align="center">Obrigatório</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Pessoa</strong></td><td align="center">Sim</td><td>Busca por nome, CPF ou NIS. Lista apenas pessoas que ainda não possuem cadastro no programa. Quando o cadastro é iniciado pelo perfil da pessoa, o campo vem pré-preenchido e bloqueado.</td></tr><tr><td><strong>Equipamento</strong></td><td align="center">Sim</td><td>Pré-preenchido com o equipamento do usuário logado. Bloqueado para técnicos comuns; editável para usuários com <code>GERACAO_RENDA_ADMINISTRAR</code> (podem cadastrar em qualquer equipamento com módulo habilitado).</td></tr><tr><td><strong>Status</strong></td><td align="center">Sim</td><td>Status inicial no programa: Ativo ou Inativo. Padrão: Ativo.</td></tr><tr><td><strong>Data de Inserção</strong></td><td align="center">Sim</td><td>Data de início da participação no programa. Não pode ser futura.</td></tr><tr><td><strong>Data de Desligamento</strong></td><td align="center">Condicional</td><td>Obrigatório quando o status é "Inativo". Deve ser posterior à data de inserção.</td></tr><tr><td><strong>Motivo de Desligamento</strong></td><td align="center">Condicional</td><td>Obrigatório quando o status é "Inativo". Selecione entre os 9 motivos disponíveis.</td></tr><tr><td><strong>Observações</strong></td><td align="center">Não</td><td>Campo de texto livre para registrar informações complementares.</td></tr></tbody></table>

### Regra de duplicidade

O sistema impede que a mesma pessoa seja cadastrada duas vezes no programa. Ao tentar, a validação bloqueará a gravação.

***

## Consultar e Editar Cadastros

A listagem centralizada de cadastros é acessada via **Programa de Geração de Renda > Cadastro**.

### Colunas da listagem

<table><thead><tr><th width="242.666748046875">Coluna</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Equipamento</strong></td><td>Equipamento de vínculo. Visível apenas para administradores.</td></tr><tr><td><strong>Pessoa</strong></td><td>Nome (social ou civil). Link direto para o perfil da pessoa.</td></tr><tr><td><strong>Status</strong></td><td>Badge colorido: verde (Ativo) ou vermelho (Inativo). Para inativos, exibe o motivo de desligamento.</td></tr><tr><td><strong>Data de Inserção</strong></td><td>Data de início no programa.</td></tr><tr><td><strong>Data do Desligamento</strong></td><td>Data de saída (oculta por padrão).</td></tr><tr><td><strong>Motivo do Desligamento</strong></td><td>Motivo da saída (oculta por padrão).</td></tr><tr><td><strong>Observações</strong></td><td>Texto de observações (oculta por padrão).</td></tr><tr><td><strong>Registrado</strong></td><td>Data e usuário de criação.</td></tr><tr><td><strong>Alterado</strong></td><td>Data e usuário da última alteração.</td></tr></tbody></table>

### Filtros disponíveis

<table><thead><tr><th width="252">Filtro</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Equipamento</strong></td><td>Filtra por equipamento. Visível apenas para administradores. Padrão: equipamento do usuário logado.</td></tr><tr><td><strong>Status</strong></td><td>Filtra por status. Padrão: "Ativo" pré-selecionado. Aceita múltipla seleção.</td></tr><tr><td><strong>Período de inserção</strong></td><td>Filtra por intervalo de datas de inserção (data início e data fim).</td></tr><tr><td><strong>Motivo de Desligamento</strong></td><td>Filtra por motivo. Aceita múltipla seleção.</td></tr><tr><td><strong>Registro excluído</strong></td><td>Permite incluir ou exibir apenas cadastros excluídos. Visível apenas para administradores.</td></tr></tbody></table>

### Acessar o cadastro da pessoa

Ao clicar em uma linha da listagem, o sistema redireciona para a **aba Programa de Geração de Renda** no perfil da pessoa, onde é possível:

* Visualizar e editar os dados do cadastro
* Excluir ou restaurar o cadastro
* Acessar e preencher os formulários PIA

### Editar cadastro

Na aba do programa no perfil da pessoa, clique em **"Editar"** na linha do cadastro. O mesmo formulário de criação é exibido com os dados atuais, permitindo alterar status, datas, motivo de desligamento e observações. O campo Pessoa fica bloqueado.

### Excluir e restaurar

* **Excluir**: remove o cadastro (soft delete). O vínculo da pessoa com o programa é desfeito.
* **Restaurar**: recupera um cadastro excluído.

***

## Plano Individual de Atendimento (PIA)

O PIA documenta o planejamento e a evolução individual de cada pessoa no programa por meio de formulários dinâmicos. É acessado pela **aba Programa de Geração de Renda** no perfil da pessoa, logo abaixo da tabela de cadastro.

### Como funciona

O PIA é composto por múltiplos formulários configurados pelo administrador na tela de Configurações. Cada formulário pode ser preenchido individualmente para cada pessoa cadastrada no programa.

### Tabela PIA

A tabela exibe todos os formulários configurados com as seguintes informações:

<table><thead><tr><th width="252.666748046875">Coluna</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Título</strong></td><td>Nome do formulário PIA.</td></tr><tr><td><strong>Status</strong></td><td>Estado atual do preenchimento.</td></tr><tr><td><strong>Registrado</strong></td><td>Data de criação e usuário que preencheu.</td></tr><tr><td><strong>Alterado</strong></td><td>Data da última alteração e usuário.</td></tr></tbody></table>

#### Status possíveis

<table><thead><tr><th width="205">Status</th><th width="144.333251953125">Cor</th><th>Significado</th></tr></thead><tbody><tr><td><strong>Preenchido</strong></td><td>Verde</td><td>Formulário preenchido na versão atual.</td></tr><tr><td><strong>Não preenchido</strong></td><td>Vermelho</td><td>Formulário ainda não foi preenchido para esta pessoa. Linha com fundo vermelho.</td></tr><tr><td><strong>Preenchido (versão desatualizada)</strong></td><td>Amarelo</td><td>Formulário foi preenchido, mas a versão configurada mudou desde então. Linha com fundo amarelo.</td></tr></tbody></table>

### Preencher um formulário PIA

1. Na tabela PIA, clique em **"Preencher"** na linha do formulário desejado
2. Um painel lateral (slide-over) abre com o formulário dinâmico
3. Preencha os campos conforme necessário
4. Clique em salvar

O botão de preencher/editar só aparece se o usuário pertencer ao mesmo equipamento do cadastro da pessoa (ou for administrador).

### Editar um formulário PIA

1. Clique em **"Editar"** na linha do formulário já preenchido
2. O painel lateral abre com os dados atuais
3. Faça as alterações necessárias
4. Ao salvar, o sistema grava automaticamente o **histórico de alterações** campo-a-campo

### Histórico de alterações

Cada campo do PIA que for alterado gera um registro de histórico contendo:

* Data da alteração
* Usuário que alterou
* Equipamento do usuário
* Valor anterior
* Valor novo

Para consultar o histórico de um campo, clique no **ícone de relógio** (hint action) ao lado do campo. Um modal exibe a tabela completa de alterações daquele campo específico.

### Visualizar

Clique em **"Visualizar"** para ver os dados preenchidos em modo somente leitura, incluindo o histórico de alterações disponível por campo.

Se o registro foi preenchido em uma versão anterior do formulário, um aviso é exibido:

> "Este registro foi preenchido em uma versão anterior do formulário. A versão configurada atualmente é diferente."

### Excluir

Disponível apenas para usuários com permissão `GERACAO_RENDA_PIA_EXCLUIR`. A exclusão é definitiva (com confirmação).

### Imprimir

Duas opções de impressão:

* **Imprimir individual**: botão na linha de cada formulário preenchido. Gera página de impressão com cabeçalho institucional, dados da pessoa e conteúdo do formulário.
* **Imprimir todos**: botão no topo da tabela PIA. Gera página de impressão unificada com todos os formulários PIA preenchidos daquela pessoa em sequência.

A impressão inclui:

* Logotipo da SMDHC
* Título "Plano Individual de Atendimento (PIA) — Programa de Geração de Renda"
* Nome da pessoa, código SIAD, equipamento e status
* Conteúdo completo do formulário organizado por seções
* Dados de auditoria (quem cadastrou, quando, última alteração)
* Data e hora da impressão
