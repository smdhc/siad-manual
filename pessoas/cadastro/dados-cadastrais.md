# Dados Cadastrais

## Visão geral

Ao continuar para a tela de cadastro, você será apresentado à primeira aba de **Dados Cadastrais** da pessoa, onde será possível coletar os <mark style="color:purple;">Dados de Identificação</mark>, como <mark style="background-color:purple;">Nome Civil</mark>, <mark style="background-color:purple;">Data de Nascimento</mark>, <mark style="background-color:purple;">Documentos</mark>, entre outros.

{% hint style="info" %}
Apesar do cadastro estar separado em 5 seções/abas, é possível terminar o preenchimento a qualquer momento, estando em qualquer seção, desde que todos os campos de preenchimento obrigatório estejam devidamente preenchidos.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>Tela de cadastro - aba "Dados Cadastrais"</p></figcaption></figure>

Atualmente são coletados os seguintes campos:

* Nome civil (obrigatório);
* Nome social
* Data de nascimento ou idade aproximada (obrigatório);
* Nome da mãe (obrigatório);
* Nome do pai
* País de Nascimento
* Município de Nascimento
* CPF (obrigatório);
* NIS
* Outros documentos.

## Sigilo de Cadastro

Ao marcar um registro como sigiloso, é necessário <mark style="background-color:$danger;">**redobrar a atenção**</mark> quanto ao tratamento das informações. Isso inclui cuidado especial com o conteúdo compartilhado e com o acesso aos dados, principalmente os relacionados a **endereço** e **contato**, que ficam automaticamente <mark style="color:red;">ocultos</mark> para todos os usuários.

Esses dados só podem ser visualizados mediante **justificativa**, respeitando as normas de proteção de informações sensíveis.

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>Sigilo do Cadastro</p></figcaption></figure>

{% hint style="warning" %}
Uma vez ativada, essa opção só poderá ser desativada pelo próprio usuário que a acionou ou pela supervisão técnica da área temática correspondente.
{% endhint %}

Ao acessar um cadastro sigiloso por meio de um outro equipamento, o sistema exibirá todas as informações normalmente, mas mostrará um alerta:

<figure><img src="../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>Aviso de cadastro sigiloso - mesma temática</p></figcaption></figure>

Além disso, os dados de **endereço** e **contato** ficam ocultos por padrão, e somente são liberados mediante justificativa:

<figure><img src="../../.gitbook/assets/image (189).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Ao registrar uma justificativa de acesso, o sistema exibirá automaticamente os dados solicitados. No entanto, tanto a identificação do usuário quanto a justificativa informada serão registradas na trilha de auditoria, podendo ser consultadas a qualquer momento para fins de controle e transparência.
{% endhint %}

{% hint style="danger" %}
⚠️ O uso indevido dessas informações está sujeito a **sanções administrativas e/ou legais**, conforme as normas internas e a legislação vigente sobre proteção de dados.
{% endhint %}

## Obrigatoriedade dos campos

{% hint style="warning" %}
Os campos de preenchimento obrigatório serão indicados pelo símbolo <mark style="color:red;">\*</mark> ao lado do nome do campo, como por exemplo, os campos de <mark style="background-color:purple;">Nome Civil</mark> e <mark style="background-color:purple;">Data de Nascimento</mark>.
{% endhint %}

Caso você tente criar o cadastro sem preencher todos os campos obrigatórios, uma mensagem em vermelho aparecerá dizendo que aquele campo é obrigatório.

<figure><img src="../../.gitbook/assets/image (104).png" alt=""><figcaption><p>Exemplo de campo obrigatório sem preenchimento</p></figcaption></figure>

## Nomes

Recomendamos que todos os campos de nomes (nome civil, social, mãe e pai) sejam cadastrados com as **primeiras iniciais em maiúsculo** e **demais letras em minúsculo**, bem como **incluir todos os acentos** existentes no nome da pessoa.

{% hint style="danger" %}
Exemplo de escrita errada: JOSE CONCEICAO DA SILVA
{% endhint %}

{% hint style="success" %}
Exemplo de escrita correta: José Conceição da Silva
{% endhint %}

Independentemente da forma utilizada no cadastro, o sistema conseguirá [pesquisar ](../pesquisa/pesquisa-global.md)tanto com minúscula/maiúscula, como com/sem acento.

## Data de nascimento desconhecida

Existem situações nas quais não é possível coletar a data de nascimento exata da pessoa. Nesses casos, o sistema permite coletar a idade aproximada. Para fazer isso, basta selecionar a opção <mark style="background-color:purple;">Data de nascimento desconhecida?</mark> e informar a <mark style="background-color:purple;">idade aproximada</mark> (autodeclarada) da pessoa.

{% hint style="info" %}
O preenchimento da data de nascimento ou idade aproximada é obrigatório, devendo ser preenchido um dos dois.
{% endhint %}

{% hint style="warning" %}
Apesar dessa possibilidade, sempre recomendamos que a data de nascimento seja informada, mesmo que em momento posterior, pois essa é uma informação essencial para análise e estudos da população atendida.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>Exemplo de preenchimento do campo "idade aproximada"</p></figcaption></figure>

## País de nascimento

Ao informar um país de nascimento que não seja o Brasil, o sistema automaticamente ocultará o campo <mark style="background-color:purple;">Município de Nascimento</mark>, pois este coleta somente informações sobre municípios brasileiros.

<figure><img src="../../.gitbook/assets/image (6) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>País de nascimento estrangeiro</p></figcaption></figure>

Da mesma forma, ao selecionar um <mark style="background-color:purple;">Município de Nascimento</mark>, o sistema automaticamente preencherá o campo <mark style="background-color:purple;">País de Nascimento</mark> como sendo <mark style="background-color:yellow;">Brasil</mark>.

<figure><img src="../../.gitbook/assets/image (7) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>Exemplo de Município de Nascimento preenchido.</p></figcaption></figure>

{% hint style="info" %}
Para facilitar a consulta, tanto o campo <mark style="background-color:purple;">País de Nascimento</mark> quanto o campo <mark style="background-color:purple;">Município de Nascimento</mark> permitem pesquisar por trechos do nome, não importando se a pesquisa foi feita utilizando palavras maiúsculas/minúsculas. Contudo, a inclusão ou exclusão dos **acentos pode impactar na pesquisa**. Caso não localize um registro, tente incluir ou excluir os acentos (por padrão, todos os municípios estão com acento).
{% endhint %}

## Múltiplos documentos

Além do CPF e NIS, o sistema também permite adicionar **outros documentos** da pessoa, como RG, RNE e outros. Para isso, basta clicar no botão <mark style="background-color:purple;">Adicionar outro documento</mark>, localizado ao final da seção <mark style="color:purple;">Documentos</mark>, selecione o <mark style="background-color:purple;">Tipo de Documento</mark> desejado e informe o número do mesmo no campo <mark style="background-color:purple;">Nº Documento</mark>.

No caso de outro tipo de documento não listado entre as opções existentes, basta selecionar a opção <mark style="background-color:purple;">Outro</mark> e, no campo <mark style="background-color:purple;">Tipo de Documento (Outro)</mark>, informar qual o nome desse tipo de documento, conforme imagem abaixo.

{% hint style="info" %}
Todos os documentos cadastrados, independentemente do tipo, poderão ser pesquisados através da [Pesquisa Global](../pesquisa/pesquisa-global.md).
{% endhint %}

Caso queira <mark style="color:red;">excluir</mark> algum documento, basta clicar no <mark style="background-color:red;">ícone de lixeira</mark> (<mark style="color:red;">vermelho</mark>) localizado à direita do documento desejado.

<figure><img src="../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>Seção de "Documentos"</p></figcaption></figure>

{% hint style="info" %}
As realidades de cada pessoa atendida podem variar muito e, desse modo, deve haver flexibilidade nos documentos aceitos para cadastro e/ou atendimento. É, portanto, importante registrar algum tipo de documento de identificação apresentado, ainda que pouco comum ou desgastado pelo tempo, se for o único que a pessoa tenha no momento. Se o documento apresentar nome do usuário e número, deve ser registrado.
{% endhint %}

## Documentos duplicados

O sistema impedirá gravar um cadastro caso o CPF informado já esteja cadastrado no sistema. O mesmo vale para o NIS.

<figure><img src="../../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>Exemplo de CPF já cadastrado</p></figcaption></figure>

## Pessoa sem CPF

Existem situações, como de imigrantes ou crianças, nas quais a pessoa não possui CPF. Nesses casos, basta habilitar a opção <mark style="background-color:purple;">Não possui CPF</mark>, e o sistema removerá a obrigatoriedade de preenchimento do mesmo.

<figure><img src="../../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>Opção "Não possui CPF"</p></figcaption></figure>

{% hint style="warning" %}
Não utilize essa funcionalidade para outras situações que não sejam as descritas acima. Isso pode dificultar a consulta desse cadastro posteriormente, podendo ocasionar <mark style="color:red;">duplicidades</mark> no sistema.&#x20;
{% endhint %}

## Edição de CPF

A partir da **versão 3.0.0** do SIAD, <mark style="background-color:red;">não</mark> será mais possível alterar o CPF de uma pessoa. Essa é uma medida que visa garantir que o mesmo cadastro não seja reutilizado por pessoas distintas, preservando assim o seu histórico.

Para os cadastros cuja opção "<mark style="background-color:purple;">Não possui CPF</mark>" tenha sido selecionada, ainda será possível alterar e completar o cadastro com o CPF da pessoa.

{% hint style="warning" %}
Caso o cadastro de uma pessoa X tenha sido criado erroneamente com o CPF de outra pessoa Y, recomendamos que o cadastro seja alterado/corrigido mantendo os dados da pessoa Y em questão, e seja criado um novo cadastro para a pessoa X.
{% endhint %}

{% hint style="info" %}
Caso tenha dúvidas sobre essa regra, entre em contato através do e-mail <mark style="color:$info;">siad@prefeitura.sp.gov.br</mark>.
{% endhint %}

## Atendimento Emergencial

Existem situações emergenciais, como a de vulnerabilidade da vítima, nas quais não é possível coletar todos os dados obrigatórios, especialmente em <mark style="color:red;">casos de emergências</mark> ou <mark style="color:red;">situações extremas</mark>. Nesses casos, é possível habilitar a opção <mark style="background-color:purple;">Atendimento emergencial de vítima de violência</mark>, localizada ao final da tela, que permitirá concluir o cadastro informando somente o **Nome Civil** e a **Data de Nascimento/Idade Aproximada**.

Além disso, ao selecionar esta opção, será aberta um campo de <mark style="background-color:purple;">Justificativa</mark>, de preenchimento obrigatório, no qual você deverá descrever o motivo do atendimento ser emergencial.

{% hint style="warning" %}
O atendimento emergencial deve ser utilizado somente em <mark style="color:red;">situações extremas</mark>! É essencial que o cadastro seja **devidamente atualizado** em momento posterior. O uso indevido dessa opção poderá ocasionar em uma série de cadastros duplicados e sem as informações necessárias para realizar o devido acompanhamento da pessoa atendida em nossa rede.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (34).png" alt=""><figcaption><p>Atendimento emergencial</p></figcaption></figure>

A seguir, abordaremos a seção de "Endereço e Contato".
