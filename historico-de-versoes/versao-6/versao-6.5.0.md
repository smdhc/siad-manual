---
description: 'Previsão de lançamento: 12/02/2026'
---

# Versão 6.5.0

A **versão 6.5.0** do SIAD é uma versão que traz melhorias e ajustes diversos.

Confira abaixo todos os detalhes dessa atualização.

## Melhorias

### Atendimentos - Importação e exportação de tipos de atendimentos

Foi disponibilzada uma funcionalidade de importação e exportação na tela de configuração dos tipos de atendimentos, permitindo migrar tipos de atendimentos entre ambientes (testes e produção, por exemplo).

### Atendimentos - Tela de acompanhamento externo

Foi disponibilizada uma configuração que permite habilitar uma tela de acompanhamento para os formulários externos.

Além disso, foi implementada a possibilidade de vincular o atendimento à pessoa posteriormente, em modo de edição.

### Cadastro de Pessoas - Transferência de Sigilo e Atividades Coletivas

Foi adicionado um novo botão "Transferir sigilo" na Ficha de Cadastro da Pessoa, visível somente para administradores e para cadastros sigilosos, com janela que permite selecionar o cadastro destino e o modo de transferência (copiar ou mover).

Além disso, agora também é possível (mediante permissão de Administrador) transferir as atividades coletivas de um cadastro duplicado para outro.

## Ajustes

### Cadastro de Pessoas - Correção de erro ao consultar cadastro

Foi corrigido um erro exibido ao tentar consultar um cadastro através da pesquisa global, no módulo "Admin".

### Cadastro de Pessoas - Correção de erro gravar novo cadastro

Foi corrigido um erro exibido ao gravar novos cadastros que possuíam CEP inválido no CadÚnico.

### Formulários externos - Ajustes diversos

Foram realizados os seguintes ajustes nas configurações do formulário externo:

* Remoção do usuário Admin da lista de profissionais;
* Checagem de visibilidade ao acessar formulário que deixou de ser externo.

### Meu Trampo - Ajustes de regras

Foram realizados ajustes diversos nas regras de funcionamento da fase de recursos do Edital Meu Trampo é Empreender.

### Transcidadania - Ajuste na sincronização de frequências

A sincronização de frequências com o cadastro do Transcidadania foi desligada na edição de frequências, e mantida somente no registro de novas frequências.
