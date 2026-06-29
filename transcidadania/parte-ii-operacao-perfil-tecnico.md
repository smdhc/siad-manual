# Parte II — Operação (perfil técnico)

## Cadastrar Pessoa Beneficiária

Para cadastrar uma nova pessoa no Programa Transcidadania, acesse **Transcidadania > Cadastro** e clique em **"Cadastrar Pessoa Beneficiária"**. Alternativamente, o cadastro pode ser iniciado diretamente pela aba Transcidadania no perfil da pessoa.

### Elegibilidade

Apenas pessoas com **identidade de gênero compatível** com o público-alvo (pessoas trans) podem ser cadastradas. O sistema valida automaticamente e restringe a busca de pessoas apenas àquelas elegíveis. Se a identidade de gênero da pessoa não se enquadrar, ela não aparecerá nos resultados de busca.

Cada pessoa pode ter apenas **um cadastro ativo** no programa. Se a pessoa já estiver cadastrada, o botão de criação não é exibido na aba Transcidadania.

### Formulário de inserção

O formulário é dividido em três seções:

#### Perfil da pessoa beneficiária

<table><thead><tr><th width="198.333251953125">Campo</th><th width="128.6666259765625" align="center">Obrigatório</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Pessoa</strong></td><td align="center">Sim</td><td>Busca por nome, CPF ou NIS. Lista apenas pessoas trans que ainda não possuem cadastro no programa. Na criação a partir do perfil da pessoa, vem pré-preenchido e bloqueado.</td></tr><tr><td><strong>Equipamento de vínculo</strong></td><td align="center">Sim</td><td>Pré-preenchido com o equipamento do usuário logado. Bloqueado na criação (lista apenas equipamentos com módulo Transcidadania habilitado).</td></tr><tr><td><strong>Área de interesse profissional</strong></td><td align="center">Sim</td><td>Seleção da área de interesse profissional da pessoa. Se "Outra" for selecionada, um campo de texto adicional é exibido para especificar.</td></tr></tbody></table>

#### Educação

<table><thead><tr><th width="218.333251953125">Campo</th><th width="135.3333740234375" align="center">Obrigatório</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Escolaridade</strong></td><td align="center">Sim</td><td>Nível de escolaridade atual. Sincroniza automaticamente com o cadastro da pessoa ao salvar.</td></tr><tr><td><strong>Elevação Escolar</strong></td><td align="center">Não</td><td>Nível em que a pessoa está cursando dentro do programa (Fundamental I, Fundamental II, Ensino Médio, Formação Técnica, Formação Superior).</td></tr><tr><td><strong>Formação escolar (especificar)</strong></td><td align="center">Condicional</td><td>Visível quando a elevação escolar é Formação Técnica ou Formação Superior. Detalhamento do curso.</td></tr><tr><td><strong>Rede Escolar</strong></td><td align="center">Sim</td><td>Rede de ensino: Municipal, Estadual, Particular ou Outra.</td></tr><tr><td><strong>Rede Escolar (outra)</strong></td><td align="center">Condicional</td><td>Visível quando rede escolar é "Outra". Especificar qual.</td></tr><tr><td><strong>Modalidade</strong></td><td align="center">Condicional</td><td>Modalidade de ensino (EJA, Regular etc.).</td></tr><tr><td><strong>Escola</strong></td><td align="center">Condicional</td><td>Visível para redes Municipal e Estadual. Seleciona escola da lista oficial. Exibe informações de contato da escola selecionada.</td></tr><tr><td><strong>Nome da Escola</strong></td><td align="center">Condicional</td><td>Visível para redes Particular e Outra. Campo de texto livre para informar o nome.</td></tr><tr><td><strong>Ano letivo de abandono/evasão escolar</strong></td><td align="center">Não</td><td>Se a pessoa abandonou a escola, indicar o ano letivo.</td></tr><tr><td><strong>Motivo do abandono/evasão escolar</strong></td><td align="center">Condicional</td><td>Obrigatório quando o ano letivo de evasão é preenchido. Opções: Bullying, Transfobia, Preconceito etc.</td></tr></tbody></table>

#### Dados do programa

<table><thead><tr><th width="218.333251953125">Campo</th><th width="140.666748046875" align="center">Obrigatório</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Status</strong></td><td align="center">Sim</td><td>Status inicial no programa (Ativo, Inativo, Suspenso, Fila de Espera Ativo/Inativo).</td></tr><tr><td><strong>Data de inserção</strong></td><td align="center">Condicional</td><td>Obrigatório quando o status não é de fila de espera. Data de início da participação no programa.</td></tr><tr><td><strong>Data de início da suspensão</strong></td><td align="center">Condicional</td><td>Obrigatório quando o status é "Suspenso". Deve ser posterior à data de inserção e anterior à data atual.</td></tr><tr><td><strong>Data de inserção na fila</strong></td><td align="center">Condicional</td><td>Obrigatório para status de fila de espera.</td></tr><tr><td><strong>Data de saída da fila</strong></td><td align="center">Condicional</td><td>Obrigatório para "Fila de Espera (Inativo)".</td></tr><tr><td><strong>Motivo da saída da fila</strong></td><td align="center">Condicional</td><td>Obrigatório para "Fila de Espera (Inativo)".</td></tr><tr><td><strong>Data de desligamento</strong></td><td align="center">Condicional</td><td>Obrigatório quando o status é "Inativo". Deve ser posterior à data de inserção.</td></tr><tr><td><strong>Motivo de desligamento</strong></td><td align="center">Condicional</td><td>Obrigatório quando o status é "Inativo". Opções: Emprego CLT, Desistência, Mudou de Município, Transferência etc.</td></tr><tr><td><strong>Agência bancária</strong></td><td align="center">Sim</td><td>Agência para recebimento do benefício. Obrigatório para status fora da fila de espera.</td></tr><tr><td><strong>Código de benefício SMDET</strong></td><td align="center">Sim</td><td>Código único do benefício na SMDET. Deve ser único no sistema.</td></tr><tr><td><strong>Observações</strong></td><td align="center">Não</td><td>Campo de texto livre.</td></tr><tr><td><strong>TCR Assinado</strong></td><td align="center">Não</td><td>Upload do Termo de Compromisso e Responsabilidade assinado.</td></tr><tr><td><strong>Documentação de inserção</strong></td><td align="center">Não</td><td>Upload de documentação complementar.</td></tr></tbody></table>

### O que acontece ao salvar

Ao gravar o cadastro, o sistema executa automaticamente:

1. Se o status for **Ativo**: adiciona o benefício "Transcidadania" ao cadastro de benefícios da pessoa
2. Se o status for diferente de Ativo: remove o benefício "Transcidadania" do cadastro da pessoa (se existir)
3. Sincroniza a **escolaridade** com o cadastro geral da pessoa (se diferente)
4. Se a transição for de "Fila de Espera (Ativo)" para "Ativo" sem data de saída da fila: preenche automaticamente a data de saída = data de inserção e motivo = "Inserção no Programa"

***

## Consultar e Editar Cadastros

A listagem de cadastros é acessada via **Transcidadania > Cadastro**. Exibe todos os cadastros do programa com sinalização visual de inconsistências.

### Colunas da listagem

<table><thead><tr><th width="205.3333740234375">Coluna</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Equipamento</strong></td><td>Equipamento de vínculo do cadastro.</td></tr><tr><td><strong>Pessoa</strong></td><td>Nome (social ou civil), código do benefício SMDET e idade. Link direto para o perfil da pessoa.</td></tr><tr><td><strong>Inserção</strong></td><td>Data de inserção no programa.</td></tr><tr><td><strong>Escola</strong></td><td>Nome da escola vinculada.</td></tr><tr><td><strong>Status</strong></td><td>Status atual no programa (com badge colorido).</td></tr><tr><td><strong>Registrado</strong></td><td>Data e usuário de criação.</td></tr><tr><td><strong>Alterado</strong></td><td>Data e usuário da última alteração.</td></tr></tbody></table>

Cadastros com inconsistências aparecem com **fundo vermelho** na listagem, acompanhados de uma legenda explicativa.

### Filtros disponíveis

<table><thead><tr><th width="252">Filtro</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Equipamento</strong></td><td>Filtra por equipamento de vínculo. Pré-selecionado com o equipamento do usuário logado. Lista apenas equipamentos com módulo Transcidadania habilitado.</td></tr><tr><td><strong>Status</strong></td><td>Filtra por status. Padrão: "Ativo" e "Suspenso" pré-selecionados. Permite múltipla seleção.</td></tr><tr><td><strong>Situação (consistência)</strong></td><td>Permite filtrar apenas inconsistentes ou apenas consistentes.</td></tr><tr><td><strong>Escolaridade</strong></td><td>Filtra pela escolaridade da pessoa.</td></tr><tr><td><strong>Rede Escolar</strong></td><td>Filtra pela rede de ensino registrada no cadastro.</td></tr><tr><td><strong>Escola</strong></td><td>Filtra pela escola vinculada.</td></tr><tr><td><strong>Motivo de desligamento</strong></td><td>Filtra por motivo de desligamento (para cadastros inativos).</td></tr><tr><td><strong>Período de inserção</strong></td><td>Filtra por intervalo de datas de inserção.</td></tr><tr><td><strong>Registro excluído</strong></td><td>Permite incluir ou exibir apenas cadastros excluídos.</td></tr></tbody></table>

### Editar cadastro

Clique no botão de edição na linha do cadastro. O mesmo formulário de inserção é exibido, com as seguintes diferenças:

* O campo **Pessoa** fica desabilitado (não é possível trocar)
* O campo **Equipamento** fica editável (permite transferir para outro equipamento com módulo habilitado)
* O campo **Status** exibe apenas as transições permitidas a partir do status atual
* Todos os campos educacionais e do programa podem ser atualizados

### Excluir e restaurar cadastros

* **Excluir**: disponível para usuários com permissão `TRANSCIDADANIA_EXCLUIR`. Somente cadastros **sem frequências registradas** podem ser excluídos.
* **Restaurar**: disponível para usuários com permissão `TRANSCIDADANIA_REATIVAR`. Permite restaurar cadastros excluídos.

***

## Registrar Frequência Mensal

O registro de frequência é o acompanhamento principal do programa, feito mensalmente para cada pessoa ativa. Há duas formas de acessar:

1. **Pela tela de acompanhamento** (Transcidadania > Acompanhamento > tabela de pendentes > botão "Registrar Frequência")
2. **Pela aba Transcidadania** no perfil da pessoa (seção de histórico de frequências)

### Formulário de frequência

#### Dados gerais

<table><thead><tr><th width="154.333251953125">Campo</th><th width="130.6666259765625" align="center">Obrigatório</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Pessoa</strong></td><td align="center">—</td><td>Exibido como referência (desabilitado).</td></tr><tr><td><strong>Equipamento</strong></td><td align="center">—</td><td>Pré-preenchido com o equipamento do usuário (desabilitado).</td></tr><tr><td><strong>Ano</strong></td><td align="center">Sim</td><td>Ano de referência da frequência.</td></tr><tr><td><strong>Mês</strong></td><td align="center">Sim</td><td>Mês de referência. Meses futuros, já registrados e fora das janelas ficam desabilitados.</td></tr><tr><td><strong>Status</strong></td><td align="center">Sim</td><td>Status da pessoa no mês (Ativo, Inativo, Suspenso). Pré-preenchido com o status da frequência anterior ou do cadastro.</td></tr></tbody></table>

#### Dados educacionais (visíveis quando status = Ativo)

<table><thead><tr><th width="181.6666259765625">Campo</th><th width="149.6666259765625" align="center">Obrigatório</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Rede Escolar</strong></td><td align="center">Sim</td><td>Pré-preenchido com dados da frequência anterior ou do cadastro.</td></tr><tr><td><strong>Escola</strong></td><td align="center">Condicional</td><td>Para redes Municipal/Estadual — seleção da lista oficial.</td></tr><tr><td><strong>Nome da Escola</strong></td><td align="center">Condicional</td><td>Para redes Particular/Outra — campo de texto.</td></tr><tr><td><strong>Elevação Escolar</strong></td><td align="center">Não</td><td>Nível em que a pessoa está cursando.</td></tr></tbody></table>

#### Frequências e cálculos (visíveis quando status = Ativo)

<table><thead><tr><th width="259.3333740234375">Campo</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Frequência Escolar (%)</strong></td><td>Percentual de frequência na escola no mês. Peso: 60% (a partir de 2025).</td></tr><tr><td><strong>Frequência em Atividades Complementares (%)</strong></td><td>Percentual de frequência em atividades do programa. Peso: 40% (a partir de 2025).</td></tr><tr><td><strong>Frequência Total Mensal (%)</strong></td><td>Calculado automaticamente pela soma ponderada. Campo desabilitado.</td></tr><tr><td><strong>Desconto</strong></td><td>Faixa de desconto calculada automaticamente com base na frequência total.</td></tr><tr><td><strong>Pagamento (R$)</strong></td><td>Valor calculado automaticamente = valor anual × (1 - desconto).</td></tr></tbody></table>

#### Dados de desligamento (visíveis quando status = Inativo)

<table><thead><tr><th width="225">Campo</th><th width="141" align="center">Obrigatório</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Data de desligamento</strong></td><td align="center">Sim</td><td>Data do desligamento.</td></tr><tr><td><strong>Motivo de desligamento</strong></td><td align="center">Sim</td><td>Motivo da saída do programa.</td></tr><tr><td><strong>Transferido para</strong></td><td align="center">Condicional</td><td>Visível quando motivo = "Transferência". Selecionar equipamento de destino.</td></tr></tbody></table>

#### Comprovantes e observações

| Campo                                       | Descrição                                                           |
| ------------------------------------------- | ------------------------------------------------------------------- |
| **Comprovante de frequência escolar**       | Upload de documento(s) comprobatório(s). Aceita múltiplos arquivos. |
| **Comprovante de frequência de atividades** | Upload de documento(s) comprobatório(s).                            |
| **Documentação adicional**                  | Upload de outros documentos relevantes.                             |
| **Observações**                             | Campo de texto livre.                                               |

### Cálculo automático

Ao preencher os percentuais de frequência, o sistema calcula em tempo real:

1. **Frequência total** = (Frequência escolar × 60%) + (Frequência atividades × 40%)
2. **Faixa de desconto** baseada na frequência total:

<table><thead><tr><th width="216">Frequência total</th><th>Desconto (a partir de 2026)</th></tr></thead><tbody><tr><td>Acima de 89%</td><td>Sem desconto</td></tr><tr><td>80% a 89%</td><td>1/30 do valor</td></tr><tr><td>70% a 79%</td><td>2/30 do valor</td></tr><tr><td>60% a 69%</td><td>3/30 do valor</td></tr><tr><td>50% a 59%</td><td>4/30 do valor</td></tr><tr><td>Abaixo de 50%</td><td>NÃO PAGAR</td></tr></tbody></table>

3. **Valor de pagamento** = Valor anual do benefício × (1 - desconto)

### Sincronização com o cadastro

Ao **registrar** uma nova frequência (não se aplica a edições) que seja referente ao mês atual ou ao mês imediatamente anterior, os seguintes dados são copiados automaticamente para o cadastro do Transcidadania:

* Status
* Motivo e data de desligamento (se aplicável)
* Rede escolar, escola, nome da escola e elevação escolar

> **Importante**: a sincronização ocorre apenas no ato do **registro**, não na **edição**. Frequências editadas após o registro não atualizam o cadastro. Eventuais divergências são sinalizadas como inconsistência de escola.

### Restrições de edição

* O técnico só pode editar/excluir frequências registradas pelo **próprio equipamento**
* A frequência precisa estar dentro de uma das janelas de preenchimento configuradas
* Administradores podem editar qualquer frequência a qualquer momento

***

## Painel de Acompanhamento (Pendentes)

O painel de acompanhamento oferece uma visão gerencial mensal, permitindo verificar rapidamente quais frequências já foram registradas e quais beneficiários estão pendentes. Acesse via **Transcidadania > Acompanhamento**.

### Filtros

<table><thead><tr><th width="153.3333740234375">Filtro</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Ano</strong></td><td>Ano de referência. Padrão: ano corrente. Listado de 2018 até o ano atual.</td></tr><tr><td><strong>Mês</strong></td><td>Mês de referência. Padrão: mês anterior ao atual.</td></tr></tbody></table>

Ao selecionar ano e mês, o sistema exibe duas tabelas.

### Tabela 1 — Frequências registradas

Exibe todos os acompanhamentos já registrados pelo equipamento do usuário para o mês selecionado. Cada linha mostra os dados da pessoa, frequências, desconto, valor e permite visualizar/editar/excluir.

### Tabela 2 — Beneficiários pendentes

Exibe as pessoas que:

* Estão com status **Ativo** no programa
* Estão vinculadas ao equipamento do usuário logado
* Foram inseridas no programa antes do mês de referência
* **Ainda não possuem** frequência registrada para o mês/ano selecionado

Cada linha possui o botão **"Registrar Frequência"** que abre diretamente o modal de registro com ano e mês pré-preenchidos.

### Informações de janela

No topo da tabela de pendentes, o sistema exibe:

* Datas da 1ª janela de preenchimento
* Datas da 2ª janela de correções
* Status atual (em andamento, encerrado, aguardando período de preenchimento, aguardando período de correção)

Cadastros com inconsistências aparecem com fundo vermelho também nesta tabela.

***

## Plano Individual de Atendimento (PIA)

O PIA documenta o planejamento e a evolução individual de cada pessoa no programa através de formulários dinâmicos. É acessado pela **aba Transcidadania** no perfil da pessoa (seção PIA).

### Como funciona

O PIA é composto por múltiplos formulários configurados pelo administrador (ex: "Dados Socioeconômicos", "Saúde", "Projeto Profissional"). Cada formulário pode ser preenchido individualmente para cada pessoa beneficiária.

### Tabela PIA

A tabela exibe todos os formulários configurados com as seguintes informações:

<table><thead><tr><th width="192">Coluna</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Título</strong></td><td>Nome do formulário PIA.</td></tr><tr><td><strong>Status</strong></td><td>Estado atual do preenchimento (veja abaixo).</td></tr><tr><td><strong>Registrado</strong></td><td>Data de criação e usuário que preencheu.</td></tr><tr><td><strong>Alterado</strong></td><td>Data da última alteração e usuário.</td></tr></tbody></table>

#### Status possíveis

<table><thead><tr><th width="217.666748046875">Status</th><th width="137">Cor</th><th>Significado</th></tr></thead><tbody><tr><td><strong>Preenchido</strong></td><td>Verde</td><td>Formulário preenchido na versão atual.</td></tr><tr><td><strong>Não preenchido</strong></td><td>Vermelho</td><td>Formulário ainda não foi preenchido para esta pessoa. Linha com fundo vermelho.</td></tr><tr><td><strong>Preenchido (versão desatualizada)</strong></td><td>Amarelo</td><td>Formulário foi preenchido, mas a versão configurada mudou desde então. Linha com fundo amarelo.</td></tr><tr><td><strong>Atualização pendente</strong></td><td>Amarelo</td><td>Formulário foi preenchido, mas já ultrapassou o prazo configurado sem ser atualizado.</td></tr></tbody></table>

### Preencher um formulário PIA

1. Na tabela PIA, clique em **"Preencher"** na linha do formulário desejado
2. Um painel lateral (slide-over) abre com o formulário dinâmico
3. Preencha os campos conforme necessário
4. Clique em salvar

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

Para consultar o histórico de um campo, clique no **ícone de relógio** ao lado do campo. Um modal exibe a tabela completa de alterações daquele campo.

### Visualizar

Clique em **"Visualizar"** para ver os dados preenchidos em modo somente leitura, incluindo o histórico de alterações disponível por campo.

Se o registro foi preenchido em uma versão anterior do formulário, um aviso é exibido no topo:

> "Este registro foi preenchido em uma versão anterior do formulário. A versão configurada atualmente é diferente."

### Excluir

Disponível para usuários com permissão `TRANSCIDADANIA_PIA_EXCLUIR`. A exclusão é definitiva (com confirmação).

### Imprimir

Duas opções de impressão disponíveis:

* **Imprimir individual**: botão na linha de cada formulário preenchido. Gera página de impressão apenas daquele formulário.
* **Imprimir todos**: botão no topo da tabela. Gera página de impressão com todos os formulários PIA preenchidos daquela pessoa em sequência.

### Permissões necessárias

<table><thead><tr><th width="291.3333740234375">Ação</th><th>Permissão</th></tr></thead><tbody><tr><td>Ver a tabela PIA</td><td><code>TRANSCIDADANIA_PIA_CONSULTAR</code></td></tr><tr><td>Preencher formulários</td><td><code>TRANSCIDADANIA_PIA_CADASTRAR</code></td></tr><tr><td>Editar formulários</td><td><code>TRANSCIDADANIA_PIA_ALTERAR</code></td></tr><tr><td>Excluir formulários</td><td><code>TRANSCIDADANIA_PIA_EXCLUIR</code></td></tr></tbody></table>
