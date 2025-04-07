---
description: 'Data de lançamento: 14/03/2025'
---

# Versão 3.1.0

A **versão 3.1.0** do SIAD é uma versão de <mark style="background-color:green;">melhorias</mark> no módulo de Projetos e diversos <mark style="background-color:blue;">ajustes</mark> no sistema em geral.

Confira abaixo todos os detalhes dessa atualização.

## Melhorias

### Atendimentos - Exibição de profissionais inativos no filtro

O filtro de profissionais na tela principal de Atendimentos passa a exibir todos os profissionais do equipamento, inclusive aqueles que já não estão mais ativos.

### Atendimentos - Novo atributo "Menor deacompanhado"

Foi adicionada uma nova opção de atributo de atendimento sincronizada com o campo "Criança/adolescente separado/desacompanhado" do Cadastro de Pessoas (exclusivo de equipamentos de imigrantes).

### Atendimentos - Melhorias nas configurações de atributos

O módulo de configurações dos formulários de atendimento foi melhorado de forma a facilitar a reordenação e configuração dos itens de listas suspensas (somente Administradores).

### Projetos - Melhorias diversas

Foram aplicadas as seguintes melhorias no módulo de Projetos:

* Exibição do período do projeto no menu lateral e no cadastro de uma nova etapa do cronograma;
* Desagrupamento dos botões de ação das etapas do cronograma;
* Inclusão de um contador visual de etapas do cronograma no menu lateral;
* Inclusão de instruções e textos explicativos na tela de cadastro do projeto;
* Exibição de alerta de projeto excluído no menu lateral;
* Possibilidade de acessar todas as telas de um projeto mesmo estando excluído;
* Inclusão do histórico de edições e alterações de projeto (somente Administradores);
* Inclusão de nova tela para configurar notificações (somente Administradores).

## Ajustes

### Atendimentos - Correção de grupos vazios

Ao registrar um atendimento através da ficha de cadastro de uma pessoa, o sistema estava exibindo grupos de atendimentos não compatíveis com o equipamento em questão, trazendo a lista de tipos de atendimento vazia. Esse comportamento foi corrigido, passando a exibir somente os grupos que possuam algum tipo de atendimento compatível.

### Atendimentos - Exclusão de tipos de atendimentos

Foi bloqueada a possibilidade de excluir um tipo de atendimento que já tenha algum atendimento, na tela de edição.

### Atendimentos - Melhorias nos filtros

O filtro "Tipo de Atendimento" foi ajustado para trazer somente os tipos de atendimentos configurados para o equipamento.

Além disso, por questões de performance, foi <mark style="background-color:red;">removida a possibilidade de listar todos os atendimentos</mark>, bem como a paginação da lista de atendimentos foi <mark style="background-color:blue;">simplificada</mark>.

Esses ajustes foram necessários para evitar a sobrecarga do sistema. Em breve serão disponibilizados painéis e relatórios que facilitarão a consolidação dos dados de atendimento.

### Cadastro de Pessoas - Exibição dos Dados de Imigração

A partir dessa versão, a seção "Dados de Imigração" da Ficha de Cadastro da Pessoa passa a ser exibida somente se houver alguma das informações preenchida.

Além disso, foi adicionada uma observação indicando que a atualização desses dados só pode ser realizada por equipamentos de imigrantes.

### Cadastro de Pessoas - Limpeza de benefícios

Foi realizada uma limpeza no campo "Outros benefícios" do cadastro de pessoas, adicionando a opção "Outros" na lista de benefícios (caso não tivesse) e passando as demais informações para o novo campo "Observações".

A partir dessa versão, a lista de outros benefícios na Ficha de Cadastro passa a ser exibida somente se a opção "Outros" for selecionada.

### Cadastro de Pessoas - Situação Emergencial de Imigrantes

Foi aplicada uma correção no cadastro de pessoas imigrantes em situação de emergência, fazendo com que apenas os campos <mark style="color:blue;">Nome</mark>, <mark style="color:blue;">Data de Nascimento</mark> e <mark style="color:blue;">País de Nascimento</mark> sejam obrigatórios nessa situação.

### Login - Correção de preenchimento automático

Corrigido erro que era apresentado na tela de login em navegadores com preenchimento automático habilitado.

A partir dessa versão, o botão para realizar o login ficará habilitado somente se o campo CPF for corretamente preenchido pelo usuário.
