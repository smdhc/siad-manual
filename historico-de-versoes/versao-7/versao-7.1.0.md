---
description: 'Data de lançamento: 16/04/2026'
---

# Versão 7.1.0

A **versão 7.1.0** do SIAD é uma versão que traz melhorias e ajustes diversos.

Confira abaixo todos os detalhes dessa atualização.

## Melhorias

### Geral - Troca de vínculo

O componente de troca de vínculo agora permite selecionar também o módulo desejado, assim como é feito na tela de login.

### Infraestrutura - Atualização do Filament

O framework utilizado para desenvolvimento do SIAD (Filament) foi atualizado para a v4.10.1.

### Projetos - Marcadores

Foi adicionado um novo campo para cadastrar "Marcadores" associados ao projeto.

### Transcidadania - Alerta de escola inconsistente

Foi adicionado um novo alerta na tela de cadastro do Transcidadania, que é exibido caso a escola do cadastro esteja diferente da informada na última frequência.

### Transcidadania - Rede Escolar (Outra) e Modalidade

O campo "Rede Escolar (Outra)" foi substituído por uma lista fechada de opções.

Além disso, foi acrescentado o campo "Modalidade" caso a Rede Escolar seja "Outra".

## Ajustes

### Benefícios - Correção de listas pesquisáveis

Foi corrigido um bug que não estava gravando corretamente as informações de atributos do tipo lista/select pesquisável.

### Cadastro de Pessoas - Correção de erro na pesquisa global

Foi corrigido o erro que era exibido ao utilizar a pesquisa global em outros módulos do sistema.

### Equipamentos - Campos logradouro e bairro

Os campos logradouro e bairro foram desbloqueados, permitindo assim sua edição.

### Meu Trampo - Correção de flag vencedora

Foi corrigido um problema na persistência da informação de proposta vencedora ao analisar a proposta.

### Projetos - Correção de textos

Foram corrigidos os textos das tabelas de projetos e etapas para refletir os novos campos de áreas corresponsáveis e áreas envolvidas.

### Projetos - Correção do botão de Indicadores

Foi corrigida a exibição do botão de Indicadores na Ficha do Projeto.

### Projetos - Correção de indicadores em atraso

Foi corrigida a verificação de indicador em atraso quando o tipo de métrica for Subprefeitura.

### Transcidadania - Correção do registro de frequência

Foi corrigido um erro, que subiu na junto da v7.0.0, que era exibido ao registrar frequência a partir da tela de Acompanhamento.

## Hotfixes

* v7.1.1: Correção na inclusão de anexos e filtros de objetivos estratégicos e resultados chave no SIAD Projetos.
