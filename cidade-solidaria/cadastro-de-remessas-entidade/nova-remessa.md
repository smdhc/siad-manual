# Nova remessa

## Acessando a tela

<figure><img src="../../.gitbook/assets/image (28).png" alt=""><figcaption></figcaption></figure>

Para cadastrar uma nova remessa, acesse o menu **“Remessas”**, onde será exibida a listagem das remessas em aberto.

Em seguida, clique no botão **“Cadastrar Remessa”** para abrir a tela de cadastro.

Para que o cadastro seja liberado, as seguintes condições precisam ser atendidas:

* Existir um ciclo de entregas vigentes (SESANA);
* A entidade estar cadastrada em um lote vigente (SESANA);
* Os dados de entrega da entidade estarem atualizados (SESANAA);
* Não existir nenhuma remessa anterior em aberto.

Caso alguma dessas condições não seja atendida, será exibida uma <mark style="background-color:$danger;">tela de erro</mark>, conforme abaixo:

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>Exemplo de erros que podem ser exibidos ao acessar a tela de cadastro.</p></figcaption></figure>

Caso a situação dependa de validação ou ação da SESANA, será necessário entrar em contato com a equipe gestora do Programa Cidade Solidária.

Se a pendência estiver relacionada a uma remessa anterior, será preciso regularizá-la antes de iniciar um novo cadastro — por exemplo, realizando a **prestação de contas** da remessa anterior.

## Cadastrar Nova Remesa

Caso todas as condições sejam atendidas, será exibida a tela para início de uma nova remessa. Nela, serão apresentados os dados cadastrais da entidade, que poderão ser atualizados conforme necessário.

<figure><img src="../../.gitbook/assets/image (3) (1).png" alt=""><figcaption><p>Exemplo de tela de cadastro de uma nova remessa</p></figcaption></figure>

No início do formulário será exibido o **Período de Preenchimento Atual**, que contém o prazo para que as entidades cadastradas nesse lote cadastrem seus beneficiários.

{% hint style="danger" %}
Após o término do período de preenchimento, não será mais possível cadastrar novas remessas.
{% endhint %}

Após preencher o formulário com todas as informações solicitadas, clique em "**Criar**", para cadastrar a remessa. Será aberta a tela de visualização da remessa, por onde será possível consultar as informações de cadastro e adicionar beneficiários.

<figure><img src="../../.gitbook/assets/image (4) (1).png" alt=""><figcaption><p>Tela de visualização da remessa</p></figcaption></figure>

Note que a Remessa é cadastrada automaticamente com o status "<mark style="background-color:blue;">**Em elaboração**</mark>". Isso significa que a remessa ainda está aberta para edições e cadastro de novos beneficiários.

## Cadastrar Beneficiários

Para adicionar pessoas beneficiárias na remessa, clique no botão "**Cadastrar Beneficiários**", localizado no canto superior direito da tela de visualização, ou no menu lateral "**Beneficiários**".&#x20;

<figure><img src="../../.gitbook/assets/image (5) (1).png" alt=""><figcaption></figcaption></figure>

Ambas as opções irão levar para a tela de listagem de beneficiários, por onde será possível consultar os beneficiários já cadastrados ou adicionar novos.

<figure><img src="../../.gitbook/assets/image (6) (1).png" alt=""><figcaption><p>Listagem de beneficiários da remessa</p></figcaption></figure>

Para adicionar uma nova pessoa, basta clicar no botão "<mark style="background-color:blue;">**Adicionar Beneficiário**</mark>".

Será aberta uma nova janela, que permitirá consultar pelo **CPF** da pessoa beneficiária.

<figure><img src="../../.gitbook/assets/image (7) (1).png" alt=""><figcaption><p>Janela para consulta de CPF de beneficiário</p></figcaption></figure>

Informe o **CPF da pessoa responsável** pelo recebimento da cesta e clique em "**Continuar**".

Nesse momento, o sistema realizará uma consulta à base do **CadÚnico** para verificar se a pessoa está apta a receber as cestas, considerando os seguintes critérios:

* Valor de renda média familiar (per capita) mensal de até **meio salário mínimo**;
* Idade maior ou igual a **18 anos**;
* Cadastro atualizado em até no máximo **2 anos**.

{% hint style="warning" %}
Caso a pessoa ou família tenha se cadastrado recentemente no CadÚnico, é possível que ainda não conste no sistema, pois há um intervalo de tempo até que a base do SIAD seja atualizada. Nessa situação, entre em contato com a equipe do Programa Cidade Solidária para obter orientações sobre como proceder.
{% endhint %}

Além dos requisitos acima, o sistema <mark style="color:$danger;">impedirá</mark> o cadastro nos seguintes casos:

* Família já cadastrada na <mark style="color:$danger;">mesma remessa</mark> (seja a pessoa pesquisada ou outro membro da família);
* Família já cadastrada por <mark style="color:$danger;">outra entidade no mesmo ciclo</mark> (não é necessário que seja a mesma pessoa).

Caso todos os requisitos sejam atendidos e a pessoa esteja apta a receber, o sistema exibirá os demais dados de identificação. Em seguida, clique em **“**<mark style="background-color:blue;">**Adicionar**</mark>**”** para prosseguir.

<figure><img src="../../.gitbook/assets/image (8) (1).png" alt=""><figcaption><p>Janela de consulta de pessoas</p></figcaption></figure>

Após adicionar, a lista de beneficiários será atualizada com a pessoa informada.

<figure><img src="../../.gitbook/assets/image (9) (1).png" alt=""><figcaption><p>Lista de beneficiários cadastrados para a remessa</p></figcaption></figure>

{% hint style="danger" %}
Após a adição de um beneficiário, a exclusão não será mais permitida. Casos excepcionais deverão ser comunicados à equipe do Programa Cidade Solidária, que avaliará e poderá realizar a exclusão.
{% endhint %}

### Limite de Cestas ou Indisponibilidade do Formulário

Caso o limite de cestas configurado para a entidade seja atingido, o sistema exibirá a mensagem abaixo e o botão "Adicionar beneficiário" ficará oculto:

<figure><img src="../../.gitbook/assets/image (11) (1).png" alt=""><figcaption></figcaption></figure>

O mesmo vale caso o lote fique indisponível por algum motivo ou o status da remessa mude.
