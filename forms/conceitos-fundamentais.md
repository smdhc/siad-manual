# Conceitos Fundamentais

## Visão geral da estrutura

O SIAD Forms organiza-se em dois grandes blocos que se complementam:

* **Formulário**: a estrutura de campos que será preenchida pelo usuário.
* **Fluxo**: o processo de trabalho que orquestra um ou mais formulários em etapas sequenciais.

Na prática, primeiro você constrói o formulário (a "folha" que será preenchida) e depois o conecta a um fluxo (o "processo" que define quem preenche, quando e em que ordem).

## Hierarquia dos Elementos

**Formulário**\
└── Versão do Formulário\
&#x20;   └── Seção\
&#x20;       └── Atributo (campo)

**Fluxo**\
&#x20;   └── Versão do Fluxo\
&#x20;       └── Etapa → vinculada a um Formulário (versão publicada)

**Protocolo** (gerado pelo preenchimento)\
└── Resposta (dados de cada etapa)

## Glossário

### Bloco do Formulário

<table><thead><tr><th width="163">Conceito</th><th>O que é</th></tr></thead><tbody><tr><td><strong>Formulário</strong></td><td>A entidade principal que agrupa a estrutura de campos. Funciona como um "modelo" reutilizável que pode ser vinculado a uma ou mais etapas de fluxos diferentes.</td></tr><tr><td><strong>Versão do Formulário</strong></td><td>Cada formulário pode ter múltiplas versões. Uma versão representa um "estado" da estrutura de campos em determinado momento. Sempre que houver alteração estrutural, precisa ser criada uma nova versão. Apenas versões publicadas podem ser vinculadas a etapas.</td></tr><tr><td><strong>Seção</strong></td><td>Agrupamento lógico de campos dentro de uma versão do formulário. Serve para organizar visualmente os campos em blocos temáticos (ex: "Dados pessoais", "Informações do projeto").</td></tr><tr><td><strong>Atributo</strong></td><td>O campo ou pergunta propriamente dita. Pode ser de diversos tipos (texto, número, data, seleção, arquivo, repeater, etc.) e possui configurações de validação, visibilidade e permissões.</td></tr></tbody></table>

### Bloco do Fluxo

<table><thead><tr><th width="168">Conceito</th><th>O que é</th></tr></thead><tbody><tr><td><strong>Fluxo</strong></td><td>O processo de trabalho completo. Define o contexto geral (nome, descrição, configurações de acesso) e agrupa suas versões.</td></tr><tr><td><strong>Versão do Fluxo</strong></td><td>Assim como o formulário, o fluxo é versionado. Cada versão define um conjunto de etapas e suas configurações. Sempre que houver mudança de etapas, deverá ser criada uma nova versão.</td></tr><tr><td><strong>Etapa</strong></td><td>Um passo dentro do fluxo. Cada etapa é vinculada a uma versão publicada de um formulário e possui configurações próprias de visibilidade, disponibilidade e permissões de acesso.</td></tr></tbody></table>

### Tipos de Etapa

<table><thead><tr><th width="170">Tipo</th><th>Comportamento</th></tr></thead><tbody><tr><td><strong>Inicial</strong></td><td>A primeira etapa do fluxo. Ao ser preenchida, gera um novo protocolo. Todo fluxo possui pelo menos uma etapa inicial.</td></tr><tr><td><strong>Intermediária</strong></td><td>Etapas subsequentes. Para serem acessadas, exigem um número de protocolo já existente. Usadas para análise, parecer, recurso, etc.</td></tr></tbody></table>

### Bloco da Execução

<table><thead><tr><th width="176">Conceito</th><th>O que é</th></tr></thead><tbody><tr><td><strong>Protocolo</strong></td><td>O registro gerado quando um usuário preenche a etapa inicial de um fluxo. Funciona como um "dossiê" que acompanha todo o processo, recebendo as respostas de cada etapa ao longo do workflow. Possui um número único de identificação.</td></tr><tr><td><strong>Resposta</strong></td><td>Os dados efetivamente preenchidos em uma etapa específica de um protocolo. Um protocolo pode ter uma resposta para cada etapa do fluxo.</td></tr></tbody></table>

## Como os conceitos se relacionam

Para ilustrar, veja um exemplo prático de um fluxo de inscrição de uma conferência:

**Formulários criados:**

* Formulário "Inscrição" (v1.0 publicada) - campos: nome, CPF, e-mail, temática de interesse
* Formulário "Análise" (v1.0 publicada) - campos: parecer, resultado (deferido/indeferido), justificativa
* Formulário "Recurso" (v1.0 publicada) - campos: argumentação, documentos anexos

**Fluxo "Conferência Municipal 2026":**

* Etapa 1 (Inicial, pública): vinculada ao formulário "Inscrição"
* Etapa 2 (Intermediária, interna): vinculada ao formulário "Análise"
* Etapa 3 (Intermediária, pública): vinculada ao formulário "Recurso"

**Execução:**

1. Maria acessa o formulário público e se inscreve → é gerado o **Protocolo #1234**
2. Um analista interno acessa o Protocolo #1234 e preenche a etapa de análise → é gravada a **Resposta** da etapa 2
3. Maria consulta o resultado pelo número do protocolo e, caso indeferida, preenche o recurso → é gravada a **Resposta** da etapa 3

## Versionamento: por que existe?

Tanto formulários quanto fluxos são versionados. Isso permite:

* **Evoluir sem quebrar**: alterar campos ou etapas sem afetar protocolos já em andamento, que continuam vinculados à versão anterior.
* **Manter histórico**: respostas gravadas permanecem íntegras, mesmo que a estrutura do formulário mude posteriormente.
* **Testar antes de publicar**: uma nova versão pode ser construída em rascunho, revisada e só então publicada.

### Ciclo de vida de uma versão do formulário

```
Rascunho → Publicada
              ↓
         (nova versão)
         Rascunho → Publicada
```

Uma versão publicada não pode ser alterada estruturalmente. Para fazer mudanças, cria-se uma nova versão.

{% hint style="warning" %}
Só pode existir uma única versão publicada, tanto para formulários quanto para fluxos.
{% endhint %}

{% hint style="info" %}
Ao editar o formulário de uma versão antiga sendo que já existe uma nova versão, será exibido o novo formulário para que o usuário possa preencher com as informações mais recentes.
{% endhint %}

## Perfis de acesso

O SIAD Forms opera com os seguintes perfis, do mais ao menos privilegiado:

<table><thead><tr><th width="184">Perfil</th><th width="156">Escopo</th><th>Resumo</th></tr></thead><tbody><tr><td><strong>Administrador do Sistema</strong></td><td>Global</td><td>Acesso total a todos os fluxos, protocolos e respostas. Não é afetado por nenhuma restrição.</td></tr><tr><td><strong>Administrador do Fluxo</strong></td><td>Por fluxo</td><td>Gerencia versões, etapas e configurações do fluxo. Pode excluir/restaurar protocolos. Não é afetado por restrições de acesso.</td></tr><tr><td><strong>Editor do Fluxo</strong></td><td>Por fluxo</td><td>Pode atualizar status e observações de protocolos. Tem acesso à todos os protocolos, independentemente das regras e restrições de acesso.</td></tr><tr><td><strong>Usuário com acesso à Etapa</strong></td><td>Por etapa</td><td>Acessa conforme as permissões configuradas na etapa (consultar, cadastrar, alterar, excluir, reativar).</td></tr><tr><td><strong>Usuário Público</strong></td><td>Etapas públicas</td><td>Preenche formulários de etapas com visibilidade "Público", sem necessidade de login.</td></tr></tbody></table>

{% hint style="info" %}
Os perfis e permissões serão detalhados na página dedicada a **Configurações de Acesso**.
{% endhint %}
