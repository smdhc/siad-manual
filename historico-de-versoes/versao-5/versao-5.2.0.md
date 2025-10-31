---
description: 'Data de lançamento: 16/10/2025'
---

# Versão 5.2.0

A **versão 5.2.0** do SIAD é uma versão que traz <mark style="background-color:blue;">melhorias e ajustes</mark> diversos no sistema em geral.

Confira abaixo todos os detalhes dessa atualização.

## Melhorias

### Cadastro de Pessoas - Integração com CadÚnico

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

Na tela de cadastro/alteração de pessoas, após o preenchimento do CPF, caso a pessoa esteja cadastrada no CadÚnico, o sistema passará a exibir um botão para a importação dos dados do CadÚnico. Essa funcionalidade permitirá preencher automaticamente os seguintes campos de cadastro:

* Nome civil
* Data de Nascimento
* Nome da mãe
* Raça/Cor
* NIS
* Endereço e Contato

{% hint style="warning" %}
No momento, essa funcionalidade encontra-se em **fase de testes** e estará restrita aos Administradores do sistema, sendo gradualmente liberada para toda a rede.
{% endhint %}

Além dessa funcionalidade, foram aplicadas as seguintes melhorias:

* Opção para cadastrar pessoa no SIAD a partir da base do CadÚnico.
* Exibição de erro ao informar CPF já cadastrado no sistema.
* Sincronização do cadastro de pessoas com CadÚnico em campos que não foram preenchidos.

### Laravel 11

O framework utilizado para o desenvolver o SIAD foi atualizado da versão 10 para a versão 11, trazendo melhorias importantes em desempenho, segurança e estabilidade. Essa nova versão torna o ambiente mais moderno e eficiente e representa um primeiro passo para atualizar os demais componentes do sistemas. Nenhuma mudança visual foi feita — tudo continua funcionando como antes, mas com uma base mais leve, segura e preparada para futuras evoluções.

### Transcidadania - Frequências de anos anteriores

Foram disponibilizados novos campo de "Frequência de Atividades Práticas" e "Frequência de Atividades Teóricas" para os registros anteriores a 2024 (regra antiga).

## Ajustes

### Cidade Solidária - Melhorias e ajustes

Foram realizados os seguintes ajustes no módulo do Programa Cidade Solidária:

* Correção de erro ao pesquisar remessa emergencial pela pesquisa global;
* Correção de erro ao tentar cadastrar remessa sem ter um ciclo vigente;
* Correção de erro ao gravar remessa (entidade);
* Correção de erro ao consultar credencial expirada;
* Inclusão e atualização de mensagens explicativas no cadastro da remessa;
* Bloqueio da edição do e-mail da entidade no cadastro da remessa.

### Edital Rango Responsa - Correção de submissão de formulário

O formulário do Edital Rango Responsa 2025 foi ajustado para impedir a submissão ao pressionar a tecla **Enter**, evitando, assim, erros que vinham ocorrendo anteriormente.

### Organizações - Correção de adapter

Corrigido o processamento de dados de CNPJ provenientes da fonte ReceitaWS.

### Transcidadania - Correção na exibição do nome da escola

Corrigido cenário em que houve alteração de rede escolar (particular para municipal, por exemplo) e o nome da escola não estava sendo atualizado.

### Usuários - Correção de usuário excluído

Corrigida a exibição do usuário de inclusão de um login, que não era exibido caso o mesmo tivesse sido excluído.
