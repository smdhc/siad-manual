---
description: 'Data de lançamento: 17/06/2025'
---

# Versão 4.5.0

A **versão 4.5.0** do SIAD é uma versão que traz <mark style="background-color:yellow;">novas funcionalidades</mark> como Encaminhamentos Recebidos, Edital FUMCAD 2025 e VI Conferência Municipal de Políticas para as Mulheres, além de <mark style="background-color:blue;">ajustes</mark> e <mark style="background-color:green;">melhorias</mark> diversas no sistema em geral.

Confira abaixo todos os detalhes dessa atualização.

## Novas funcionalidades

### Encaminhamentos Recebidos

<figure><img src="../../.gitbook/assets/image (183).png" alt=""><figcaption></figcaption></figure>

Implementada nova "aba" na Central de Encaminhamentos que permitirá que visualizar todos os encaminhamentos realizados por outros equipamentos da Rede de Atendimento SMDHC, destinados ao equipamento logado.

### Edital FUMCAD 2025

Finalizada a implementação de formulário substituto para inscrições do Edital FUMCAD 2025.

### VI Conferência Municipal de Políticas para as Mulheres

Disponibilizado novo formulário para pré-inscrição do evento VI Conferência Municipal de Políticas para as Mulheres, que ocorrerá nos dias 12/07 e 13/07/2025.

### API de Equipamentos - GeoJSON

Liberada nova versão da API de equipamentos com suporte à exportação dos dados da rede de atendimento da SMDHC no formato GeoJSON, visando aplicações de geoprocessamento.

## Melhorias

### Cadastro de Organizações - Consulta de CNPJ

Implementada funcionalidade que permite a consulta automatizada dos dados de uma entidade a partir do seu CNPJ.

## Ajustes

### Atendimentos - Correção na exibição de campos históricos

Corrigida a exibição dos atributos de atendimentos que deixaram de ser exibidos após serem vinculados a um novo atributo pai.

### Cadastro de Pessoas - Correção na duplicidade de documentos

Aplicada nova regra que impossibilita que um mesmo cadastro possua dois documentos idênticos/duplicados.

### Cadastro de Usuários - Correção de paginação e performance

Ajustado o limite de exibição de usuários na tela de consulta a fim de prevenir erros e degradação de desempenho quando a opção 'Todas' era utilizada.
