# Cadastrar Entidades

## Cadastro da Organização

<figure><img src="../../.gitbook/assets/image (194).png" alt=""><figcaption></figcaption></figure>

Para cadastrar uma nova entidade, acesse o menu "**Cadastro/Organizações**" e clique no botão "<mark style="background-color:blue;">**Cadastrar Organização**</mark>".

<figure><img src="../../.gitbook/assets/image (195).png" alt=""><figcaption></figcaption></figure>

Preencha com o CNPJ desejado e clique na lupa ao lado.

O sistema irá tentar buscar os dados da entidade automaticamente através das APIs ReceitaWS, CNPJa e BrasilAPI.

Caso tenha sucesso, os dados de identificação, endereço e contato da entidade serão automaticamente preenchidos, permitindo editar ou complementar com dados adicionais.

{% hint style="info" %}
A entidade poderá atualizar seus dados cadastrais a cada nova remessa.
{% endhint %}

Clique no botão "<mark style="background-color:blue;">**Criar**</mark>" no final da página para finalizar o cadastro.

Após gravar, você será redirecionado para a Ficha de Cadastro da Organização.

<figure><img src="../../.gitbook/assets/image (196).png" alt=""><figcaption></figcaption></figure>

Por meio dessa tela, é possível:

* Consultar os dados cadastrais da entidade;
* Alterar os dados da entidade;
* Consultar a lista de equipamentos que essa entidade gerencia;
* <mark style="color:$warning;">Manter credenciais de acesso\*;</mark>
* <mark style="color:$warning;">Atualizar os dados de entrega\*;</mark>
* <mark style="color:$warning;">Definir um limite de cestas\*;</mark>
* Consultar o histórico de remessas.

_<mark style="color:$warning;">\*obs: obrigatório para habilitar a entidade no Programa.</mark>_

## Credenciais de Acesso

Para criar uma senha de acesso ao SIAD para a entidade, clique no menu "**Credenciais de Acesso**" e no botão "<mark style="background-color:$primary;">**Cadastrar Credencial de Acesso**</mark>".

Essa etapa é fundamental para que a entidade consiga acessar o sistema.

<figure><img src="../../.gitbook/assets/image (197).png" alt=""><figcaption></figcaption></figure>

Será aberta uma janela que permitirá definir:

* quais módulos a entidade terá acesso (no momento somente a opção "Programa Cidade Solidária" está disponível);
* expiração de senha (opcional);
* observações diversas.

<figure><img src="../../.gitbook/assets/image (198).png" alt=""><figcaption></figcaption></figure>

Selecione o módulo "Programa Cidade Solidária", <mark style="background-color:$warning;">**copie a senha**</mark> e clique em "<mark style="background-color:$primary;">**Salvar**</mark>".

{% hint style="danger" %}
Após o salvamento, não será mais possível recuperar a senha criada para a entidade. Em caso de perda, será necessário reiniciar ou gerar uma nova credencial de acesso.
{% endhint %}

{% hint style="info" %}
A entidade poderá acessar o sistema através do endereço [http://siad.prefeitura.sp.gov.br/osc](http://siad.prefeitura.sp.gov.br/osc), informando eu CNPJ e a senha cadastrada através dessa tela.
{% endhint %}

### Reinicio de senha

Para reiniciar uma senha, basta abrir o menu de opções da credencial cadastrada e clicar em "<mark style="background-color:$primary;">**Reiniciar Senha**</mark>".

<figure><img src="../../.gitbook/assets/image (200).png" alt=""><figcaption></figcaption></figure>

Após a confirmação, a nova senha será exibida em um popup no canto superior direito da tela.

<figure><img src="../../.gitbook/assets/image (201).png" alt=""><figcaption></figcaption></figure>

### Exclusão de acesso

Para excluir o acesso da entidade, basta selecionar a credencial desejada e clicar em "<mark style="background-color:$danger;">**Excluir**</mark>".

<figure><img src="../../.gitbook/assets/image (202).png" alt=""><figcaption></figcaption></figure>

## Dados de Entrega

Mesmo com acesso ao sistema, a entidade não poderá cadastrar novas remessas caso os dados de entrega não estejam cadastrados.

Para cadastrar, acesse o menu "**Dados de Entrega**", localizado na seção "SESANA - Cidade Solidária".

<figure><img src="../../.gitbook/assets/image (203).png" alt=""><figcaption></figcaption></figure>

Nesta tela, informe os dados de endereço manualmente ou, se forem os mesmos da entidade, clique no botão "<mark style="background-color:$primary;">**Copiar Endereço da Entidade**</mark>" e clique em "<mark style="background-color:$primary;">**Gravar**</mark>".

{% hint style="info" %}
Somente a equipe da SESANA poderá atualizar os dados de entrega da entidade.
{% endhint %}

## Limite de Cestas

Ainda na tela de atualização dos dados de entrega, é possível definir um limite máximo de cestas que a entidade selecionada poderá receber por remessa.

Após atingido o limite, a entidade não conseguirá mais adicionar novos beneficiários na remessa.

Para que não haja nenhum limite, basta definir como "0" (zero).

Não esqueça de clicar em "<mark style="background-color:$primary;">**Gravar**</mark>" para que as alterações tenham efeito.

{% hint style="warning" %}
As configurações terão efeito apenas para as novas remessas e beneficiários cadastrados após o salvamento das alterações.
{% endhint %}
