---
description: 'Data de lançamento: 15/06/2026'
---

# Versão 8.3.0

## Melhorias

### Atendimentos - Exibição dos filtros

Os filtros da tela de atendimentos passarão a ser exibidos por padrão.

### Atendimentos - Ocupação do profissional

A listagem de atendimentos passa a exibir a ocupação dos profissionais do atendimento.

### Autenticação - Correção de Passkeys

Corrigido o endpoint `.well-known/passkey-endpoints` para retornar as URLs reais de cadastro e gerenciamento de passkeys, incluindo headers de CORS adequados.

### Cadastro de Pessoas - Aba "Pessoas atendidas"

Adiciona uma nova aba **"Atendidas neste equipamento"** na tela de Pessoas (módulo de Atendimento).

### SIAD Benefícios - Configurações de campos de pessoa

Disponibilizado novo menu "Configurações gerais" no sidebar da tela de edição do benefício, permitindo definir quais campos do cadastro de pessoas são exibidos na ficha do beneficiário.

### SIAD Benefícios - Filtros em colunas dinâmicas

Foi adicionado filtro nas colunas dinâmicas da listagem de beneficiários, assim como a possibilidade de reordená-los.

### SIAD Forms - Melhorias

Foram realizadas as seguintes melhorias no SIAD Forms:

* Habilitada a formatação de cores no RichEditor do conteúdo de e-mail das notificações.
* Adicionada action "Editar Atributo" na tabela de atributos da seção, permitindo editar o atributo diretamente sem abrir a configuração da seção.
* Adicionada exibição do ID da etapa na tabela de etapas e na aba de identificação do gerenciamento.
* Adicionada coluna "# Notificações" na tabela de etapas, contabilizando as regras configuradas (oculta por padrão).
* Implementado callout de alerta (danger) ao acessar um protocolo excluído, além de fundo vermelho nas tabelas de protocolos e respostas para registros excluídos.
* Permitida a edição de etapas em versões de fluxos publicadas que ainda não possuem respostas registradas.
* Adicionada coluna "Configurado em" no resumo de versões da infolist de formulários, exibindo os fluxos e benefícios associados.
* Adicionadas seções de "Configurações de Acesso" e "Configurações de Notificações" na infolist do fluxo (visíveis somente quando houver configuração).
* Implementada geração automática de slug (label + UUID) ao cadastrar um novo atributo, com chave desabilitada na edição.
* Adicionados atributos do tipo CEP e E-mail nas listas de preenchimento automático ao configurar atributos CNPJ e E-mail na seção.
* Bloqueada a atualização de protocolos excluídos, ocultando todas as actions das etapas (editar, imprimir, atualizar dados etc.).
* Adicionada coluna "Seções" com link "Configurar seções" no resumo de versões da infolist de formulários.
* Adicionado quadro "Resumo das Versões" na infolist de fluxos, exibindo versões cadastradas com link para gerenciar etapas.
* Implementada action "Baixar todos os anexos (ZIP)" na infolist do protocolo ao acessar dados de uma etapa (visível somente quando houver arquivos).
* Adicionado toggle "Único" na configuração de atributo na seção, que valida e impede o cadastro de formulários com valores duplicados para o mesmo atributo na mesma etapa.

### Transcidadania - Impressão do PIA

Foram adicionados novos botões que permitem realizar a impressão dos formulários do PIA Transcidadania.

## Ajustes

### Atendimentos - Exibição de profissionais na atividade coletiva

A lista de profissionais no registro de atendimentos de atividades coletivas foi corrigida de forma a exibir somente profissionais ativos na data do atendimento.

### Atendimentos - Otimização de performance

Foram realizados alguns ajustes na tela de listagem dos atendimentos visando melhorar a performance da tela.

### CadÚnico - Correção de erro de importação

Foi corrigido um erro que era exibido ao tentar importar a pessoa do CadÚnico para o cadastro de pessoas do SIAD a partir da tela do CadÚnico.

### SIAD Forms - Correções e ajustes diversos

Foram realizados os seguintes ajustes no SIAD Forms:

* Adiciona novas merge tags no sistema de notificações do Forms, permitindo personalizar e-mails com dados do destinatário, do fluxo/etapa e do equipamento do usuário que cadastrou.
* Agrupamento de botões de ação nas telas de seções e atributos.
* Corrigido problema ao gravar formulário com cor de fundo configurada.
* Corrigido problema na impressão de respostas que começavam na segunda página.
* O tamanho do logotipo da SMDHC nos e-mails foi ajustado.
* Corrigido o label dos atributos na seleção de destinatários por atributos nas configurações de notificação da etapa.
* Corrigido o cálculo do atributo "Pontuação" ao utilizar média ponderada, que agora calcula corretamente por seção antes de agregar entre seções.
* Corrigida a pesquisa de protocolo na tela de acompanhamento que retornava "not found" (aplicado trim no número informado).
* Corrigido o clique no registro da tabela de fluxos que não abria a visualização.
* Corrigida a pesquisa de usuários nas configurações de acesso (fluxo e etapa) para buscar simultaneamente por nome, e-mail e CPF (com e sem pontuação).
* Corrigida a acentuação do campo "Habilitar impressão do protocolo" na edição do fluxo.
* Corrigido o comportamento ao trocar a chave pai de uma seção: o campo de opções pai agora é limpo automaticamente.

### Usuários - Duplicação na reativação

Foi corrigido comportamento que permitia reativar um usuário excluído gerando duplicidade de vínculos ativos no mesmo equipamento.
