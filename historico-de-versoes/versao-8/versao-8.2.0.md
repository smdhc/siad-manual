---
description: 'Data de lançamento: 02/06/2026'
---

# Versão 8.2.0

A **versão 8.2.0** do SIAD é uma versão que traz melhorias e ajustes diversos.

Confira abaixo todos os detalhes dessa atualização.

## Novas funcionalidades

### PIA Transcidadania

Foi implementada nova funcionalidade no Transcidadania que permite construir e disponibilizar os formulários do PIA Transcidadania (Plano Individual de Atendimento) dentro do cadastro da pessoa.

## Melhorias

### Autenticação - Criação automática de chaves de acesso

A partir dessa versão, ao realizar o login com CPF e senha, o sistema tentará criar automaticamente uma chave de acesso para o usuário.

### Cadastro de Equipamentos - Marcadores

Foi adicionado um novo campo "Marcadores" no Cadastro de Equipamentos, permitindo associar equipamentos à "tags", facilitando assim a filtragem em painéis. A API também foi atualizada para exportar esse dado.

### SIAD Forms - Melhorias

Foram realizadas as seguintes melhorias no SIAD Forms:

* Cadastro de novos protocolos a partir do próprio SIAD.
* Componentes de CEP e CNPJ.
* Configuração de banners e cores do formulário.
* Gerenciamento de notificações.
* Impressão em lote.
* Sistema de pontuação.
* Validação de datas.

## Ajustes

### Atendimentos - Erro ao consultar atendimento em outros módulos

Foi corrigido um erro exibido ao consultar qualquer atendimento a partir do módulo Admin.

### Atendimentos - Correção de erro ao editar com regra de idade mínima

Foi corrigido um erro exibido ao tentar editar um atendimento cujo tipo possua regra de idade mínima.

### Autenticação - Auditoria de passkeys

A trilha de auditoria para as tentativas de acesso utilizando chaves de acesso (passkeys) foi melhorada.

### Benefícios - Correção de status

Foi corrigido o comportamento que permitia continuar visualizando benefícios com status rascunho ou arquivado.

### SIAD Forms - Ajustes

Foram realizados os seguintes ajustes no SIAD Forms:

* Correção de erro ao imprimir protocolo com Repeater.
* Revisão do layout de impressão.
* Correção de erro ao cadastrar etapa sem status padrão.

### Projetos - Alteração de nome de campos

O campo "Responsável" na lista de áreas corresponsáveis da etapa foi renomeado para "Pessoa Corresponsável".

## Hotfix

* v8.2.1: correção de erro ao tentar adicionar um novo atributo a um tipo de atendimento.
