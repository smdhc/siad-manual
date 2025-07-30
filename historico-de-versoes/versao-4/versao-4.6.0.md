---
description: 'Data de lançamento: 31/07/2025'
---

# Versão 4.6.0

A **versão 4.6.0** do SIAD é uma versão que traz <mark style="background-color:yellow;">novas funcionalidades</mark> como o Cadastro de Profissionais e a versão definitiva do Selo Igualdade Racial 2025, além de <mark style="background-color:blue;">ajustes</mark> e <mark style="background-color:green;">melhorias</mark> diversas no sistema em geral.

Confira abaixo todos os detalhes dessa atualização.

## Novas funcionalidades

### Cadastro de Profissionais

<figure><img src="../../.gitbook/assets/image (186).png" alt=""><figcaption></figcaption></figure>

Foi liberada uma nova funcionalidade no menu "**Cadastros > Profissionais**", permitindo a consulta dos profissionais já cadastrados no sistema.

Além disso, agora é possível registrar informações sobre ocupação e conselho de classe, que serão utilizadas futuramente em funcionalidades como atendimentos e encaminhamentos.

{% hint style="warning" %}
Para cadastrar novos profissionais no sistema ou solicitar a atualização dos dados cadastrais, o gestor do equipamento deverá enviar uma solicitação para o e-mail **siad@prefeitura.sp.gov.br**, informando os seguintes dados: nome completo, CPF, e-mail individual, ocupação e, se aplicável, o conselho de classe.
{% endhint %}

### Programa Selo Igualdade Racial 2025

Disponibilizada a versão definitiva do formulário para inscrição do Programa Selo Igualdade Racial 2025, que abrirá suas inscrições em agosto/25.

## Melhorias

### Atendimentos - Alteração da regra de sigilo

Registros de atendimentos marcados como sigilosos agora são exibidos apenas no equipamento em que foram cadastrados. Anteriormente, esses registros apareciam em todos os equipamentos, mas com os detalhes inacessíveis.

### Atendimentos - Exibição de profissionais

A lista de profissionais no registro de atendimentos passará a exibir, além do nome, a ocupação e o conselho de classe, quando cadastrados.

### Atendimentos - Otimização de performance

O formulário de atendimento (popup) foi otimizado para melhorar o desempenho, especialmente na visualização de detalhes de atendimentos históricos, que apresentavam lentidão.

### Geral - Atualização do logotipo da SMDHC

O logotipo da SMDHC foi atualizado para a nova identidade visual da PMSP.

### Infraestrutura - Aumento do limite de memória

Identificamos alguns casos no registro de atendimentos (geralmente ao registrar uma atividade coletiva) a ocorrência de telas pretas sem nenhuma mensagem de erro. Tal situação era ocasionada pelo estouro de memória individual que o sistema reserva para cada usuário/processo. Para evitar isso, foi aumentado o limite de memória por processo de usuário, de 128M para 512M, bem como demais otimizações no módulo de atendimento.

### Transcidadania - Nova janela de correções

<figure><img src="../../.gitbook/assets/image (187).png" alt=""><figcaption></figcaption></figure>

Foram criadas novas configurações no módulo Acompanhamento que permitirão definir uma nova janela/período para que os equipamentos possam realizar correções nas frequências mensais. Essa nova janela será configurada pela Coordenação de Políticas LGBTI+ e o novo período ficará visível na tela de acompanhamento.

### Transcidadania - Novo filtro de Escolaridade

Foi adicionado um novo filtro de "Escolaridade" na tela de cadastros do Transcidadania.

## Ajustes

### API - Correção de coordenadas na API de Equipamentos

Foi corrigida a exibição das coordenadas geográficas na API de equipamentos, no formato GeoJSON, que anteriormente impedia a importação dos dados em ferramentas de geoprocessamento, como o QGIS.

### Atendimentos - Filtro de Grupos e Tipos de Atendimentos

Os filtros "Grupo de Atendimento" e "Tipo de Atendimento", presentes tanto na listagem geral de atendimentos quanto no histórico da pessoa, foram ajustados para exibir apenas:

* No caso da listagem geral: os grupos e tipos de atendimento configurados para o equipamento;
* No caso do histórico da pessoa: os grupos e tipos de atendimento que já constam no histórico da pessoa.

### Cadastro de Pessoas - Edição de cadastros sigilosos

Foi restaurada a possibilidade de editar os dados de identidade, imigração e atendimento emergencial em cadastros marcados como sigilosos.

### Comunicados - Correção do contador

Foi corrigido o cálculo do contador de comunicados não lidos, que, em determinadas situações, exibia valores negativos ou incompatíveis com a quantidade real de comunicados.

### Transcidadania - Correção da lista de pendências

Foi corrigido um cenário em que pessoas eram exibidas indevidamente na lista de pendências da tela de Acompanhamento, em meses anteriores à sua inserção no programa.
