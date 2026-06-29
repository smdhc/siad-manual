# Configurar Tipos de Atendimentos

## Introdução

Os tipos de atendimento definem quais atividades podem ser registradas pelos técnicos no módulo de Atendimento. Cada tipo representa uma ação específica (ex: "Atendimento Individual", "Oficina Coletiva", "Acolhimento", "Encaminhamento para Rede") e pode ter campos personalizados, regras de visibilidade e configurações próprias.

Para gerenciar os tipos de atendimento, acesse **Atendimento > Tipos de Atendimentos**.

***

## Criar um Tipo de Atendimento

Clique em **Criar** no topo da listagem. O formulário está dividido em seções.

### Dados Básicos

<table><thead><tr><th width="159">Campo</th><th width="130" align="center">Obrigatório</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Nome</strong></td><td align="center">Sim</td><td>Nome identificador do tipo de atendimento. Deve ser único. Será exibido na seleção ao registrar atendimentos. Ex: "Atendimento Individual", "Oficina de Capacitação".</td></tr><tr><td><strong>Grupo</strong></td><td align="center">Sim</td><td>Grupo de atendimento ao qual o tipo pertence. Permite organizar tipos em categorias (ex: "Atendimento Socioassistencial", "Promoção de Direitos", "Atividades Coletivas").</td></tr><tr><td><strong>Descrição</strong></td><td align="center">Não</td><td>Texto descritivo sobre o tipo de atendimento. Visível apenas na configuração.</td></tr><tr><td><strong>Data inicial</strong></td><td align="center">Sim</td><td>Data a partir da qual o tipo de atendimento estará disponível para registro. Atendimentos fora deste período não podem ser cadastrados. Padrão: 01/01/2000.</td></tr><tr><td><strong>Data final</strong></td><td align="center">Sim</td><td>Data até a qual o tipo estará disponível. Padrão: 31/12/2100. Útil para tipos sazonais ou com vigência limitada.</td></tr><tr><td><strong>Visibilidade</strong></td><td align="center">Sim</td><td>Controla quem pode ver e utilizar este tipo de atendimento (veja detalhes abaixo).</td></tr><tr><td><strong>Permitir sigilo?</strong></td><td align="center">Não</td><td>Quando ativado, permite que atendimentos deste tipo sejam marcados como sigilosos. Atendimentos sigilosos ficam com acesso restrito.</td></tr><tr><td><strong>Prazo em dias para edição</strong></td><td align="center">Não</td><td>Limita o período em que um atendimento pode ser editado ou excluído após o registro. Conta a diferença entre a data atual e a data do atendimento. Se o equipamento ou grupo possuir prazo próprio, o que for mais restritivo prevalece.</td></tr></tbody></table>

### Visibilidade

A visibilidade define quem pode acessar e registrar atendimentos deste tipo:

<table><thead><tr><th width="180.666748046875">Opção</th><th>Comportamento</th></tr></thead><tbody><tr><td><strong>Público</strong></td><td>Visível para todos os equipamentos <strong>por padrão</strong>. É possível adicionar exceções (equipamentos que NÃO devem ver) na aba de Visibilidade.</td></tr><tr><td><strong>Restrito</strong></td><td>Oculto para todos os equipamentos <strong>por padrão</strong>. É possível adicionar exceções (equipamentos que DEVEM ver) na aba de Visibilidade.</td></tr><tr><td><strong>Interno</strong></td><td>Visível somente para Administradores do sistema. Usado para tipos de atendimento gerenciais ou de uso exclusivo da coordenação.</td></tr><tr><td><strong>Externo</strong></td><td>Habilita o formulário público (tratado na página "<a href="formularios-externos.md">Formulários Externos de Atendimento</a>").</td></tr></tbody></table>

#### Configurar exceções de visibilidade

Para tipos com visibilidade **Público** ou **Restrito**, a aba **Visibilidade** (relation manager) permite adicionar regras por:

* **Equipamento**: equipamento específico
* **Tipo de Equipamento**: todos os equipamentos de determinado tipo (ex: todos os CRAS)
* **Temática do Equipamento**: todos os equipamentos de determinada temática (ex: Assistência Social)

Para o tipo **Público**, as exceções REMOVEM o acesso (lista negra). Para o tipo **Restrito**, as exceções CONCEDEM o acesso (lista branca).

***

## Configurar Seções e Atributos

Tipos de atendimento podem ter **campos personalizados** (atributos) que serão preenchidos ao registrar o atendimento. Os atributos são organizados em seções.

### Criar seções

Na seção **Controles de visibilidade** do formulário de edição, utilize o campo **Seções**:

* Digite o nome da seção e pressione **Enter**
* Adicione quantas seções forem necessárias
* Reordene por arraste
* Ex: "Dados da Ação", "Encaminhamentos", "Observações"

Defina também o **Nº Colunas** (padrão: 3) que controla o grid do formulário de atendimento.

### Adicionar atributos

Após salvar, acesse a aba **Atributos** na tela de edição. Clique em **"Adicionar atributo"**.

<table><thead><tr><th width="218.3333740234375">Campo</th><th width="126" align="center">Obrigatório</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Atributo</strong></td><td align="center">Sim</td><td>Selecione um atributo existente do cadastro global ou crie um novo pelo botão "+".</td></tr><tr><td><strong>Seção</strong></td><td align="center">Sim</td><td>Selecione a seção onde o atributo será exibido.</td></tr><tr><td><strong>Ordem</strong></td><td align="center">Não</td><td>Posição numérica dentro da seção.</td></tr><tr><td><strong>Chave Pai</strong></td><td align="center">Não</td><td>Informe a chave de outro atributo para tornar este campo condicional.</td></tr><tr><td><strong>Opções Pai</strong></td><td align="center">Não</td><td>Quais valores do campo pai acionam a exibição deste campo.</td></tr><tr><td><strong>Obrigatório?</strong></td><td align="center">Não</td><td>Torna o preenchimento obrigatório.</td></tr><tr><td><strong>Múltiplo?</strong></td><td align="center">Não</td><td>Permite seleção de múltiplos valores.</td></tr><tr><td><strong>Largura total?</strong></td><td align="center">Não</td><td>O campo ocupa toda a largura do grid.</td></tr><tr><td><strong>Visibilidade na tabela?</strong></td><td align="center">Não</td><td>Exibe o valor como coluna na listagem de atendimentos deste tipo.</td></tr><tr><td><strong>Somar à quantidade?</strong></td><td align="center">Não</td><td>Visível para campos numéricos (Inteiro). Soma o valor informado ao campo "Quantidade" do atendimento automaticamente.</td></tr><tr><td><strong>Pesquisável</strong></td><td align="center">Não</td><td>Visível para tipos que aceitam pesquisa. Permite buscar atendimentos pelo valor deste campo na listagem.</td></tr><tr><td><strong>Quebrar linha</strong></td><td align="center">Não</td><td>Força o campo a iniciar em nova linha no formulário.</td></tr></tbody></table>

***

## Controles de Visibilidade dos Campos

A seção **Controles de visibilidade** configura quais campos padrão do atendimento estarão disponíveis:

### Campo Pessoa

<table><thead><tr><th width="232">Configuração</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Campo "Pessoa" visível?</strong></td><td>Habilita o campo de vinculação de pessoa ao atendimento. Quando desativado, o atendimento é registrado sem vínculo com pessoa (útil para ações coletivas).</td></tr><tr><td><strong>Campo "Pessoa" obrigatório?</strong></td><td>Torna obrigatória a vinculação.</td></tr><tr><td><strong>Idade mínima</strong></td><td>Restringe o cadastro a pessoas com idade mínima (validação no momento do registro).</td></tr><tr><td><strong>Idade máxima</strong></td><td>Restringe o cadastro a pessoas com idade máxima.</td></tr></tbody></table>

### Campo Profissional

<table><thead><tr><th width="261.3333740234375">Configuração</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Campo "Profissional" visível?</strong></td><td>Exibe o campo para indicar qual profissional realizou o atendimento. Lista profissionais do equipamento do usuário logado.</td></tr><tr><td><strong>Campo "Profissional" múltiplo?</strong></td><td>Permite selecionar mais de um profissional (útil para atendimentos em dupla/equipe).</td></tr><tr><td><strong>Campo "Profissional" obrigatório?</strong></td><td>Torna a seleção obrigatória.</td></tr></tbody></table>

### Campo Quantidade

<table><thead><tr><th width="242">Configuração</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Campo "Quantidade" visível?</strong></td><td>Exibe o campo de quantidade. Útil para registrar múltiplas unidades em um único atendimento (ex: 50 kits distribuídos).</td></tr><tr><td><strong>Quantidade mínima</strong></td><td>Valor mínimo aceito. Padrão: 1.</td></tr><tr><td><strong>Quantidade máxima</strong></td><td>Valor máximo aceito. Padrão: 1.</td></tr></tbody></table>

### Campo Pessoas (Quantidade)

<table><thead><tr><th width="258.6666259765625">Configuração</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Campo "Pessoas (Qtde)" visível?</strong></td><td>Exibe o campo para informar o total de pessoas atendidas/participantes (independentemente de estarem cadastradas no sistema). Comum em atividades coletivas.</td></tr><tr><td><strong>Pessoas mínimo</strong></td><td>Valor mínimo aceito. Padrão: 1.</td></tr><tr><td><strong>Pessoas máximo</strong></td><td>Valor máximo aceito.</td></tr></tbody></table>

***

## Restrição por Ocupação

A aba **Ocupações** (relation manager) permite restringir o tipo de atendimento por ocupação profissional. Quando configurada:

* Somente profissionais com a ocupação vinculada poderão registrar atendimentos deste tipo
* Se nenhuma ocupação for vinculada, qualquer profissional pode registrar

Exemplo: vincular "Assistente Social" e "Psicólogo" a um tipo de atendimento individual, impedindo que administrativos registrem esse tipo.

***

## Exemplos Práticos de Configuração

### Atendimento Individual (Socioassistencial)

<table><thead><tr><th width="238">Configuração</th><th>Valor</th></tr></thead><tbody><tr><td>Nome</td><td>Atendimento Individual</td></tr><tr><td>Grupo</td><td>Atendimento Socioassistencial</td></tr><tr><td>Visibilidade</td><td>Público</td></tr><tr><td>Pessoa visível?</td><td>Sim</td></tr><tr><td>Pessoa obrigatório?</td><td>Sim</td></tr><tr><td>Profissional visível?</td><td>Sim</td></tr><tr><td>Profissional obrigatório?</td><td>Sim</td></tr><tr><td>Quantidade visível?</td><td>Não</td></tr><tr><td>Seções</td><td>Dados do Atendimento, Encaminhamentos</td></tr><tr><td>Atributos</td><td>Motivo do Atendimento (Lista), Providências Tomadas (Texto Longo), Encaminhamentos (Lista Múltipla)</td></tr></tbody></table>

### Oficina Coletiva

<table><thead><tr><th width="239.3333740234375">Configuração</th><th>Valor</th></tr></thead><tbody><tr><td>Nome</td><td>Oficina Coletiva</td></tr><tr><td>Grupo</td><td>Atividades Coletivas</td></tr><tr><td>Visibilidade</td><td>Público</td></tr><tr><td>Pessoa visível?</td><td>Não</td></tr><tr><td>Profissional visível?</td><td>Sim</td></tr><tr><td>Profissional múltiplo?</td><td>Sim</td></tr><tr><td>Quantidade visível?</td><td>Sim (min: 1, max: 1)</td></tr><tr><td>Pessoas (Qtde) visível?</td><td>Sim (min: 1, max: 999)</td></tr><tr><td>Seções</td><td>Dados da Atividade</td></tr><tr><td>Atributos</td><td>Tema da Oficina (Texto Curto), Descrição (Texto Longo), Local (Texto Curto)</td></tr></tbody></table>

### Distribuição de Insumos (Restrito)

<table><thead><tr><th width="262.6666259765625">Configuração</th><th>Valor</th></tr></thead><tbody><tr><td>Nome</td><td>Distribuição de Insumos</td></tr><tr><td>Grupo</td><td>Promoção de Direitos</td></tr><tr><td>Visibilidade</td><td>Restrito</td></tr><tr><td>Exceções (aba Visibilidade)</td><td>Equipamento: CPD Centro, CPD Sul</td></tr><tr><td>Pessoa visível?</td><td>Não</td></tr><tr><td>Profissional visível?</td><td>Sim</td></tr><tr><td>Quantidade visível?</td><td>Sim (min: 1, max: 9999)</td></tr><tr><td>Seções</td><td>Registro</td></tr><tr><td>Atributos</td><td>Tipo de Insumo (Lista), Quantidade Distribuída (Inteiro, Somar à quantidade)</td></tr></tbody></table>

***

## Considerações

* Alterações em tipos de atendimento já utilizados afetam o formulário de registro a partir daquele momento, mas **não alteram atendimentos já gravados** (os dados dinâmicos ficam preservados no JSON do atendimento).
* Os atributos são compartilhados com o SIAD Forms — um atributo criado aqui pode ser reutilizado em formulários de outros módulos.
* O campo **"Somar à quantidade"** é útil quando se deseja calcular automaticamente o total a partir de subcontagens nos atributos (ex: somar kits masculinos + kits femininos = quantidade total).
* Tipos com visibilidade **Restrito** são ideais para atendimentos específicos de determinados equipamentos ou temáticas, sem expor para toda a rede.
* O **prazo de edição** em dias pode ser combinado com prazos configurados no equipamento ou grupo de atendimento. O sistema aplica o prazo mais restritivo entre os três.
