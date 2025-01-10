---
description: 'Data de lançamento: 10/01/2025'
---

# Versão 2.1.0

A **versão 2.1.0** do SIAD é uma versão que traz consigo o **Formulário de Regularização do Programa Cidade Solidária**, além de pequenas melhorias no Cadastro de Pessoas.

Confira abaixo todos os detalhes dessa atualização.

## Formulário de Regularização - Cidade Solidária

O ambiente do SIAD foi aproveitado para disponibilizar um novo formulário de regularização de beneficiários do Programa Cidade Solidária, por permitir uma série de validações e integração com outras bases.

Dessa forma, essa passa a ser a primeira funcionalidade do sistema que não está necessariamente atrelada à rede de atendimento da SMDHC, bem como o primeiro formulário público do sistema, que não requer que o usuário esteja autenticado.

Esse formulário será utilizado pelas entidades credenciadas no Programa Cidade Solidária para que regularizem os beneficiários com documento inválido.

<figure><img src="../.gitbook/assets/image (128).png" alt=""><figcaption><p>Formulário de Regularização de Beneficiários do Cidade Solidária</p></figcaption></figure>

Além do formulário público, também foram implementadas no módulo <mark style="background-color:purple;">Admin</mark>:

* Tela para importação da base de beneficiários (para regularização);
* Tela para acompanhamento das solicitações de regularização.

## Melhorias na consulta de CEP

Foram realizadas as seguintes melhorias na pesquisa de CEP, do <mark style="background-color:purple;">Cadastro de Pessoas</mark>:

* Validação ao pesquisar por CEP vazio;
* Inclusão de máscara para permitir somente números;
* Validação de quantidade de dígitos do CEP ao gravar o cadastro;
* Erros passam a ser exibidos no próprio campo do CEP;
* Distrito volta a ser exibido em caso de CEP inválido.

<figure><img src="../.gitbook/assets/image (129).png" alt=""><figcaption><p>Exemplo de validação de CEP</p></figcaption></figure>

Vale reforçar que a consulta de CEP é uma <mark style="background-color:orange;">etapa auxiliar</mark>, podendo ainda assim o usuário não utilizar dessa ferramenta e informar manualmente os dados de endereço.

Outro ponto a destacar é que futuramente implementaremos uma forma para que o Distrito seja preenchido automaticamente também. Por enquanto, o mesmo precisa ser informado manualmente.

## Correção de permissionamento dos botões da tela inicial

Foi corrigido o permissionamento dos botões <mark style="color:purple;">Registrar Atendimento</mark> e <mark style="color:purple;">Cadastrar Pessoa</mark> na tela inicial, que estavam sendo exibidos mesmo se o usuário não tivesse permissão específica.

<figure><img src="../.gitbook/assets/image (131).png" alt=""><figcaption><p>Botões da tela inicial</p></figcaption></figure>

A mesma revisão foi aplicada nas seguintes telas/funcionalidades:

* Botão <mark style="color:purple;">Ver Atendimentos</mark> no Cadastro de Pessoas;
* Botão <mark style="color:purple;">Registrar atendimentos</mark> na Ficha de Cadastro da Pessoa;
* Menu <mark style="color:purple;">atendimentos</mark> na Ficha de Cadastro da Pessoa;
* Exibição do indicador de atendimentos do Painel de Controle;
* Permissionamento do botão <mark style="color:purple;">Editar</mark> e menu <mark style="color:purple;">Atualizar dados</mark> da Ficha de Cadastro da Pessoa.

## Novos filtros no Cadastro de Pessoas

Foram adicionados os seguintes filtros no Cadastro de Pessoas:

* Criança/adolescente separado/desacompanhado (somente temática Imigrantes);
* Pessoas com anexos.

<figure><img src="../.gitbook/assets/image (132).png" alt=""><figcaption><p>Novos filtros no Cadastro de Pessoas</p></figcaption></figure>

## Correção da exibição dos contatos no Cadastro de Pessoas

Foi corrigida a exibição dos contatos na listagem do Cadastro de Pessoas, que estava exibindo apenas os contatos adicionais. Agora, o sistema passa a exibir tanto o contato principal quanto os contatos adicionais.

<figure><img src="../.gitbook/assets/image (133).png" alt=""><figcaption><p>Exibição de contatos na listagem de pessoas</p></figcaption></figure>

## Lista de equipamentos pesquisável nos Encaminhamentos

Ao realizar um <mark style="background-color:purple;">encaminhamento externo</mark> para outro equipamento da nossa rede de atendimento SMDHC, o sistema exibia uma lista estática de equipamentos, que dificultava a pesquisa. Agora é possível **filtrar** por partes do nome do equipamento.

<figure><img src="../.gitbook/assets/image (134).png" alt=""><figcaption><p>Nova pesquisa de equipamentos no encaminhamento externo</p></figcaption></figure>
