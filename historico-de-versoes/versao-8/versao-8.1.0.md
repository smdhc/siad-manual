---
description: 'Data de lançamento: 26/05/2026'
---

# Versão 8.1.0

A **versão 8.1.0** do SIAD é uma versão que traz melhorias e ajustes diversos.

Confira abaixo todos os detalhes dessa atualização.

## Melhorias

### Autenticação - Criação automática de chaves de acesso

A partir dessa versão, ao realizar o login com CPF e senha, o sistema tentará criar automaticamente uma chave de acesso para o usuário.

### SIAD Forms - Melhorias

Foram implementadas as seguintes melhorias no SIAD Forms:

* Possibilidade de configurar permissões a usuários externos em etapas internas.
* Criação de novos atributos de formulário:
  * Equipamento Logado;
  * Usuário Logado.
* Refatoração do formulário de edição da etapa.
* Impressão de protocolos e respostas.
* Possibilidade de configurar título e subtítulo nos formulários, bem como a revisão do modo consulta.
* Possibilidade de ocultar etapas no modo consulta, caso o usuário não possua permissão.

## Ajustes

### Encaminhamentos - Tamanho da fonte obrigatório

O campo "Tamanho da Fonte" passou a ser obrigatório, evitando o erro que ocorria ao tentar gravar sem esse campo informado.

### SIAD Forms - Ajustes

Foram realizados os seguintes ajustes no SIAD Forms:

* Correção de listagem de respostas com protocolos configurados com restrição de acesso.
* Corrigida a pesquisa de atributos pela chave.

## Hotfixes

* v8.1.1: Correção de erro ao cadastrar etapa no SIAD Forms.
