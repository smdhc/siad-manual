# Lotes

## Cadastro de Lotes

Os lotes funcionam como um mecanismo de controle, determinando quais entidades podem cadastrar remessas e em quais períodos.

Para cadastrar um novo lote, primeiramente é necessário acessar a ficha de cadastro de um **Ciclo**. Isso pode ser feito conforme descrito na [seção anterior](ciclos.md).

Na tela da Ficha de Cadastro do Ciclo, os lotes podem ser configurados utilizando o botão ‘<mark style="background-color:blue;">**Cadastrar Lotes**</mark>’ ou pelo menu lateral ‘**Lotes**’.

<figure><img src="../../.gitbook/assets/image (204).png" alt=""><figcaption></figcaption></figure>

Será aberta uma nova tela contendo a lista de lotes cadastrados para o ciclo selecionado.

Para cadastrar um novo lote, clique em "<mark style="background-color:blue;">**Cadatrar Lote**</mark>".

<figure><img src="../../.gitbook/assets/image (206).png" alt=""><figcaption></figcaption></figure>

Será aberta uma janela para informar o nome (opcional) do lote, período e observações adicionais.

Preencha com os dados solicitados e clique em "<mark style="background-color:blue;">**Criar**</mark>".

{% hint style="info" %}
Ao contrário dos ciclos, é permitido que vários lotes se sobreponham no mesmo período. Entretanto, o período de cada lote deve estar contido dentro do ciclo correspondente.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (207).png" alt=""><figcaption></figcaption></figure>

## Configurar Entidades

Para configurar as entidades que farão parte do lote, clique na coluna de entidades do lote desejado ou no menu "**Cadastrar entidades**", conforme imagem abaixo.

<figure><img src="../../.gitbook/assets/image (208).png" alt=""><figcaption></figcaption></figure>

Será aberta uma nova tela contendo a lista de entidades já cadastradas para o lote selecionado.

Para adicionar uma nova entidade, clique no botão "<mark style="background-color:blue;">**Adicionar Entidades**</mark>".

<figure><img src="../../.gitbook/assets/image (209).png" alt=""><figcaption></figcaption></figure>

Ao abrir a janela, será possível realizar a inclusão utilizando **dois métodos** distintos:

* Pesquisa individual de entidade;
* Lista de CNPJs.

### Pesquisa individual de entidade

A primeira forma consiste em utilizar o seletor de entidades assim que a janela é aberta.

Clique no campo "Entidade" para abrir a lista suspensa de entidades cadastradas no SIAD. Através dessa lista, é possível pesquisar pelo CNPJ ou Razão Social.

{% hint style="warning" %}
Somente serão listadas as entidades que estiverem cadastradas no SIAD e com dados de entrega atualizados.
{% endhint %}

Apesar da pesquisa ser individual, esse componente permite selecionar múltiplas entidades de uma vez.

<figure><img src="../../.gitbook/assets/image (210).png" alt=""><figcaption></figcaption></figure>

Este método é adequado para um número reduzido de entidades. Entretanto, para adicionar um grande volume, recomenda-se utilizar o método alternativo descrito a seguir.

### Lista de CNPJs

A segunda forma de inclusão consiste em copiar uma lista de CNPJs (um por linha).

Para utilizar esse método, clique na opção "<mark style="background-color:$primary;">**Alternar para modo de lista**</mark>", cole a lista de CNPJs (com ou sem formatação) e clique em "<mark style="background-color:blue;">**Gravar**</mark>".

<figure><img src="../../.gitbook/assets/image (211).png" alt=""><figcaption></figcaption></figure>

Ao gravar sem realizar a validação da lista, o sistema incluirá apenas as entidades aptas para cadastro no lote. Para identificar previamente CNPJs não aptos, utilize o botão ‘<mark style="background-color:blue;">**Validar Lista**</mark>’, que exibirá, logo abaixo, apenas os CNPJs que não puderam ser adicionados.

<figure><img src="../../.gitbook/assets/image (212).png" alt=""><figcaption></figcaption></figure>

Serão considerados CNPJs inaptos aqueles que:

* não forem válidos;
* não estiverem cadastrados no SIAD;
* não possuírem dados de entrega;
* já estarem cadastrados no mesmo ciclo;
* entre outros.

### Cópia de entidades

Para facilitar o cadastramento de entidades em ciclos futuros, onde provavelmente os lotes serão os mesmos, é possível utilizar o método anterior (Lista de CNPJs) combinado com o mecanismo de cópia de entidades.

Selecione o **lote de origem** que deseja copiar e, na tela de entidades, clique no botão "<mark style="background-color:blue;">**Copiar Entidades**</mark>".

<figure><img src="../../.gitbook/assets/image (213).png" alt=""><figcaption></figcaption></figure>

Ao fazer isso, o sistema automaticamente irá copiar a lista de todos os CNPJs cadastrados no lote atual para a **área de transferência** do seu computador.

<figure><img src="../../.gitbook/assets/image (214).png" alt=""><figcaption></figcaption></figure>

Para colar, acesse o **lote destino** desejado e realize os passos descritos na [seção anterior](lotes.md#lista-de-cnpjs).

### Exclusão de Entidades

Para excluir uma entidade de um lote, basta clicar em "<mark style="background-color:$danger;">**Excluir**</mark>", na linha correspondente.

{% hint style="warning" %}
O sistema somente permitirá excluir entidades que ainda não tenham cadastrado remessa no lote selecionado.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (215).png" alt=""><figcaption></figcaption></figure>

### Habilitação de remessas

O sistema habilitará automaticamente o cadastro de remessas para a entidade assim que a data atual estiver contida no período configurado para o lote em questão.

Uma vez que a entidade esteja cadastrada no lote vigente, o cadastro de remessas ficará disponível para a mesma.

Através da lista de entidades também é possível acompanhar o andamento, através das colunas "**Status da Remessa**" e "**# Cestas**".

<figure><img src="../../.gitbook/assets/image (216).png" alt=""><figcaption></figcaption></figure>
