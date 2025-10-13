# Definições

## Ciclo

Corresponde a um período de referência no qual se realizam as entregas de cestas básicas para todas as entidades participantes do programa.&#x20;

Cada ciclo poderá ser composto por um ou mais lotes, organizadas de forma escalonada ou paralela, conforme a estratégia de execução.&#x20;

A duração média de um ciclo é de 2 a 3 meses, podendo variar de acordo com o número total de pessoas beneficiárias cadastradas nos lotes correspondentes.&#x20;

{% hint style="warning" %}
O ciclo também será utilizado como critério de controle, impedindo que uma mesma família receba mais de uma cesta básica dentro do mesmo período de vigência.&#x20;
{% endhint %}

## Lote

Representa um subconjunto temporal e operacional dentro de um ciclo, vinculado a um grupo específico de entidades previamente selecionadas, que serão habilitadas para cadastrar suas remessas.&#x20;

O conceito de lote foi criado com o objetivo de escalonar a liberação do formulário de remessa, permitindo uma **implementação controlada e gradual**, em pequenos grupos de entidades.&#x20;

O cadastro de pessoas beneficiárias estará restrito ao período de vigência do lote e será permitido apenas às entidades associadas àquele lote.&#x20;

É possível haver múltiplos lotes ativos simultaneamente em um mesmo ciclo, e <mark style="background-color:$danger;">**uma mesma entidade não poderá ser vinculada a mais de um lote**</mark>.&#x20;

Todo lote deverá ser validado/encerrado por meio de permissão específica (SESANA), o que bloqueará qualquer edição em suas remessas, e fará com que o status das remessas seja alterado para “<mark style="background-color:$primary;">Aguardando entrega</mark>”. Esse status poderá ser revertido caso ainda não haja nenhum acusamento de recebimento da entrega.&#x20;

Cada lote poderá assumir os seguintes **status**:&#x20;

<table><thead><tr><th width="172">Status</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Ativo</strong></td><td>Lote que está programado para acontecer ou que está em andamento. Para que as entidades possam cadastrar remessas, é necessário que o lote esteja Ativo.</td></tr><tr><td><strong>Inativo</strong></td><td>Lote indisponível para cadastramento de remessas (por algum motivo). Esse status pode ser utilizado, por exemplo, para <mark style="background-color:$danger;">desativar temporariamente</mark> o cadastro de novas remessas de uma forma rápida.</td></tr><tr><td><strong>Encerrado</strong></td><td>Status assumido após a equipe do Programa Cidade Solidária realizar ajustes e validar o lote. Após isso, não será mais possível realizar qualquer tipo de mudança no lote. Ao encerrar, todas as remessas daquele lote mudarão de status para "Aguardando entrega".</td></tr></tbody></table>

## Remessa

Corresponde ao registro formal da solicitação de cestas básicas por parte de uma entidade, a ser realizada dentro de um lote ativo à qual ela esteja vinculada. A remessa é o **principal instrumento de coleta de dados** cadastrais e de definição do quantitativo a ser entregue.&#x20;

Cada remessa será composta por duas seções:&#x20;

* Atualização dos dados cadastrais da entidade;&#x20;
* Lista de pessoas beneficiárias elegíveis.&#x20;

Todas as remessas são iniciadas sem dados previamente preenchidos (sem reaproveitamento de remessas anteriores).

{% hint style="success" %}
É a partir das remessas que o SIAD irá disponibilizar um arquivo de exportação para que sejam geradas as ordens de serviço (fora do SIAD) para entrega das cestas.
{% endhint %}

As remessas poderão assumir os seguintes status operacionais:

<table><thead><tr><th width="199">Status</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Em elaboração</strong></td><td>Remessa criada já com os dados cadastrais da entidade e locais de entrega, com ou sem beneficiários informados. A remessa permanecerá neste status até que a equipe do Programa Cidade Solidária conclua eventuais ajustes e encerre o lote.</td></tr><tr><td><strong>Aguardando entrega</strong></td><td>A remessa foi validada e/ou teve seu lote encerrado. A partir desse momento não será mais possível alterar os dados cadatrais da remessa. <mark style="background-color:$success;">Esse é o status recomendado para exportação dos dados visando emissão das ordens de serviço.</mark><br>Nesse status é liberada a opção para que a entidade <strong>acuse o recebimento</strong> da cesta, o que liberará a prestação de contas.</td></tr><tr><td><strong>Aguardando prestação de contas</strong></td><td>Situação em que a entidade já recebeu as cestas, devendo realizar a prestação de contas, indicando individualmente quais famílias receberam as cestas.<br>A entidade só poderá cadastrar uma nova remessa (em outro ciclo) caso não haja pendências em prestação de contas anteriores.</td></tr><tr><td><strong>Excesso de tentativas</strong></td><td>Situação em que houve duas devoluções consecutivas, conforme previsto em Portaria.</td></tr><tr><td><strong>Indeferido</strong></td><td>Bloqueio da remessa por algum motivo, como CNPJ em situação irregular.</td></tr><tr><td><strong>Cancelado</strong></td><td>Seria o equivalente à exclusão de uma remessa, definida somente pela equipe do Programa Cidade Solidária. As remessas canceladas não serão consideradas nas demais validações do Programa.</td></tr><tr><td><strong>Encerrado</strong></td><td>A prestação de contas foi concluída pela entidade, encerrando formalmente a remessa.</td></tr><tr><td><strong>Encerrado com pendências</strong></td><td>a prestação de contas foi concluída pela entidade, mas o total de cestas entregues não bate com o número de cestas recebidas.</td></tr></tbody></table>

{% hint style="info" %}
Enquanto o lote estiver "Ativo", a equipe do Programa Cidade Solidária poderá alterar livremente o status das remessas.
{% endhint %}

## Remessa Emergencial

Corresponde a uma remessa avulsa, gerada exclusivamente pela equipe do Programa Cidade Solidária ou por usuários com permissão específica, destinada ao atendimento de situações emergenciais previstas em Portaria.

As remessas emergenciais podem ser cadastradas para qualquer entidade, inclusive aquelas que não estejam vinculadas ao lote vigente ou que não possuam acesso ativo ao sistema. Também é possível cadastrá-las sem a vinculação a uma entidade específica.

As remessas emergenciais não estão sujeitas à prestação de contas.

No cadastro da remessa emergencial, é obrigatório informar o quantitativo de cestas a serem entregues, o qual não precisa corresponder à lista de beneficiários.

{% hint style="info" %}
A remessa emergencial estará diretamente relacionada a um ciclo de entrega, e não a um lote.&#x20;
{% endhint %}

{% hint style="warning" %}
Toda remessa emergencial precisará ser justificada.&#x20;
{% endhint %}

## Pessoa beneficiária

É o(a) representante de uma família contemplada com a entrega de uma cesta básica, no contexto de uma remessa vinculada a um lote específico dentro de um ciclo.

Somente serão aceitas pessoas cadastradas no **Cadastro Único para Programas Sociais do Governo Federal (CadÚnico)**, maiores de 18 anos, com perfil de vulnerabilidade correspondente às faixas de pobreza I e II (renda de até meio salário mínimo), e cujo cadastro tenha sido atualizado há, no máximo, 2 anos.

Cada família poderá ter **apenas um representante** cadastrado por ciclo, independentemente da entidade ou do lote. O representante poderá ser qualquer membro da composição familiar.

Os casos em que as remessas forem indeferidas ou canceladas não serão considerados para fins de validação de famílias já cadastradas no ciclo.

O sistema impede o cadastro de CPFs ou famílias duplicadas, informando automaticamente em qual entidade e lote a pessoa ou família já está registrada.

Cada pessoa beneficiária tem direito a apenas uma cesta por ciclo/remessa.

Todas as pessoas incluídas nas remessas são registradas automaticamente no Cadastro de Pessoas do SIAD, com controle de vínculo por ciclo. A partir desse cadastro, é possível visualizar todo o histórico de cestas entregues à pessoa.

Uma vez adicionada uma pessoa a uma remessa, não será mais possível removê-la, exceto mediante permissão específica e enquanto o lote correspondente não tiver sido encerrado.

Não haverá verificação cruzada com bases de beneficiários anteriores ao novo sistema. A validação será realizada exclusivamente com a base CadÚnico vigente no mês da entrega.

## Entidade

É a organização da sociedade civil (OSC) cadastrada para participar do Programa Cidade Solidária, responsável pelo envio das remessas de cestas.

As entidades são cadastradas por meio do módulo de Organizações do SIAD. O sistema permite a emissão de uma senha individual para cada entidade, que garante acesso restrito ao módulo de cadastro de remessas.

Cada entidade pode acessar o sistema para atualizar seus dados cadastrais, cadastrar listas de beneficiários e acompanhar o status de suas remessas.

O bloqueio de uma entidade no programa pode ser realizado mediante a remoção da senha de acesso ou pela exclusão da entidade de um lote.

Também é possível configurar um limite de cestas por entidade.

{% hint style="info" %}
Compete à equipe do Programa Cidade Solidária o cadastramento e a atualização dos dados das entidades e das entregas.
{% endhint %}

## Prestação de Contas

É a etapa posterior ao recebimento das cestas, na qual a entidade deve informar quais beneficiários receberam as cestas.

Para cada beneficiário, deve ser registrado um dos seguintes status: **“**<mark style="background-color:$success;">**Entregue**</mark>**”** ou **“**<mark style="background-color:$danger;">**Não entregue**</mark>**”**.

* Caso todas as cestas previstas tenham sido entregues, o status da remessa passará para **“**<mark style="background-color:blue;">**Encerrado**</mark>**”**.
* Caso exista ao menos uma cesta não entregue, o status da remessa passará para **“**<mark style="background-color:$warning;">**Encerrado com pendências**</mark>**”**.

{% hint style="info" %}
As remessas emergenciais não estão sujeitas à prestação de contas.
{% endhint %}
