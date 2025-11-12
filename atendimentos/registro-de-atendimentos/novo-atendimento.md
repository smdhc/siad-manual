# Novo atendimento

## Fluxo básico

Ao iniciar um novo atendimento (conforme visto em "[Como acessar?](como-acessar.md)"), será aberta uma janela com uma única opção para selecionar o <mark style="color:purple;">Grupo de atendimento</mark>. Essa seleção é necessária para que seja exibida uma lista contendo somente os tipos de atendimentos pertinentes à ação desejada.

<figure><img src="../../.gitbook/assets/image (16) (1) (1).png" alt=""><figcaption><p>Seleção do grupo de atendimento</p></figcaption></figure>

Após selecionar o grupo desejado, será aberta a lista de opções contendo os **Tipos de Atendimentos** configurados para o seu equipamento.

{% hint style="info" %}
A lista de tipos de atendimento pode variar de acordo com a <mark style="color:blue;">temática</mark> do seu equipamento e as <mark style="color:blue;">regras estabelecidas pela SMDHC</mark>.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (15) (1) (1).png" alt=""><figcaption><p>Seleção do tipo de atendimento</p></figcaption></figure>

Após selecionar o tipo de atendimento desejado, será habilitado o restante do formulário, contendo as informações complementares configuradas para o tipo selecionado.

{% hint style="info" %}
Como mencionado anteriormente, o formulário será <mark style="color:blue;">adaptado conforme o tipo de atendimento selecionado</mark>, não havendo um padrão fixo de campos, exceto pelo conjunto mínimo de dados.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (17) (1) (1).png" alt=""><figcaption><p>Formulário completo de atendimento</p></figcaption></figure>

Ao terminar de preencher, clique no botão <mark style="background-color:orange;">Gravar</mark> para encerrar o registro do atendimento.

O sistema fechará a janela e voltará para a tela anterior.

Caso queira registrar um novo atendimento sem fechar a janela, basta clicar no botão <mark style="background-color:orange;">Salvar e criar outro</mark>.

## Correção do tipo de atendimento

Observe que, ao selecionar um tipo de atendimento, o sistema irá desativar o campo, como forma de prevenir a ocorrência de alguns erros. Caso você tenha selecionado um <mark style="color:blue;">Tipo de Atendimento</mark> errado e queira mudar, basta mudar o <mark style="color:purple;">grupo de atendimento</mark> ou <mark style="color:purple;">fechar e abrir novamente a janela</mark> de atendimento.

<figure><img src="../../.gitbook/assets/image (18) (1) (1).png" alt=""><figcaption><p>Altere o grupo ou reabra a janela caso tenha selecionado um tipo de atendimento errado</p></figcaption></figure>

## Data/hora do atendimento

Quando um tipo de atendimento é selecionado, o sistema preenche automaticamente o campo <mark style="color:purple;">Data/Hora do Atendimento</mark> com a data e hora atuais. Se estiver registrando um atendimento realizado no passado, basta ajustar o valor diretamente nesse campo.

{% hint style="warning" %}
O sistema não permitirá informar datas de atendimento futuras ou muito antigas.
{% endhint %}

## Seleção da pessoa atendida

Ao selecionar um tipo de atendimento individual, será exibido um campo para informar a pessoa atendida. Por padrão, esse campo apresenta as <mark style="color:blue;">últimas pessoas cadastradas</mark> em seu equipamento. Para buscar outras pessoas, você pode realizar a pesquisa por:

* Nome civil
* Nome social
* Código SIAD
* CPF

{% hint style="info" %}
Caso registre um novo atendimento por meio do Cadastro de Pessoas, o campo virá desabilitado e já preenchido com os dados da pessoa em questão.
{% endhint %}

## Seleção dos profissionais

Os tipos de atendimento que exigem dados dos profissionais envolvidos exibem um campo para a sua seleção. A lista apresentada inclui todos os <mark style="color:blue;">usuários cadastrados</mark> no equipamento com login e senha. Para localizar um profissional específico, basta <mark style="color:purple;">pesquisar pelo nome</mark>.

{% hint style="info" %}
Caso o profissional não esteja cadastrado, será necessário solicitar o seu cadastramento para o e-mail **siad@prefeitura.sp.gov.br**, informando o <mark style="color:blue;">nome completo</mark>, <mark style="color:blue;">CPF</mark> e <mark style="color:blue;">e-mail individual</mark>.
{% endhint %}

Futuramente disponibilizaremos a funcionalidade para que os próprios equipamentos possam cadastrar seus profissionais, sem a necessidade de enviar e-mail.

## Sigilo do atendimento

Em alguns tipos de atendimento, está disponível a opção de <mark style="background-color:orange;">Sigilo do Atendimento</mark>.&#x20;

Por padrão, com o **sigilo desativado**, os detalhes do atendimento serão visíveis para <mark style="color:blue;">todos os equipamentos da mesma temática</mark>.

_<mark style="color:orange;">Por exemplo: os detalhes de um atendimento realizado em um CRPIR (Igualdade Racial) estarão acessíveis a outros CRPIRs. No entanto, para um CRCM (Mulheres), apenas o registro do evento será visível, sem os detalhes.</mark>_

Com o **sigilo habilitado**, somente o <mark style="color:blue;">equipamento que registrou o atendimento</mark> poderá visualizar os detalhes.

Essas regras ainda serão submetidas a uma revisão de segurança da informação. Por enquanto, aplica-se o que está descrito no quadro abaixo:

| Sigilo     | Mesma temática                                   | Outra temática                                   |
| ---------- | ------------------------------------------------ | ------------------------------------------------ |
| Desativado | <mark style="color:green;">Ver detalhes</mark>   | <mark style="color:red;">Somente registro</mark> |
| Habilitado | <mark style="color:red;">Somente registro</mark> | <mark style="color:red;">Somente registro</mark> |

{% hint style="info" %}
Uma vez ativada, essa opção só poderá ser desativada pelo <mark style="color:blue;">próprio usuário</mark> que a acionou ou pela <mark style="color:blue;">supervisão técnica</mark> da área temática correspondente.
{% endhint %}

{% hint style="danger" %}
Por motivos de segurança, os registros de atendimentos realizados pelos **Núcleos da Ouvidoria de Direitos Humanos** (NDH) <mark style="color:red;">não serão visíveis</mark> para equipamentos de outras temáticas.
{% endhint %}

## Integração com Cadastro de Pessoas

Alguns campos, como a <mark style="color:purple;">Situação Migratória</mark> (no caso de Imigrantes) estão sincronizados com o **Cadastro de Pessoas**.

Dessa maneira, ao selecionar a pessoa, esse campo será <mark style="color:blue;">automaticamente preenchido</mark> com as informações existentes no cadastro.&#x20;

Se o campo for alterado, a atualização será refletida diretamente no cadastro da pessoa.

Esse tipo de integração possibilitará o acompanhamento da alteração dessa informação ao longo do tempo, por meio do histórico de atendimentos, além de permitir a visualização da informação mais recente no cadastro da pessoa.
