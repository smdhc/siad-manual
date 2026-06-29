# Configurar Notificações do Fluxo

## Introdução

As notificações do fluxo permitem alertar automaticamente pessoas ou equipes quando determinados eventos ocorrem nos protocolos. Essa configuração fica na seção **Notificações** ao editar um fluxo (menu lateral SIAD Forms > Fluxos > selecionar o fluxo > Editar).

> **Nota**: as notificações configuradas aqui se aplicam a eventos no **nível do protocolo** (alteração de status, exclusão e restauração). Para notificações disparadas quando uma **resposta é registrada em uma etapa específica**, configure diretamente nas notificações da etapa.

***

## Habilitar notificações

O primeiro passo é ativar o toggle **Habilitar notificações**. Enquanto desativado, nenhuma notificação será disparada independentemente das regras cadastradas.

Ao ativar, o botão **Adicionar regra** ficará disponível para configurar as regras de envio.

***

## Anatomia de uma regra de notificação

Cada regra define: como enviar, para quem enviar, e em quais situações. Os campos são:

**Tipo de envio**

<table><thead><tr><th width="137.333251953125">Opção</th><th>Comportamento</th></tr></thead><tbody><tr><td><strong>E-mail</strong></td><td>Envia um e-mail para os destinatários configurados. Permite personalizar remetente, assunto e conteúdo.</td></tr><tr><td><strong>Sistema</strong></td><td>Envia uma notificação interna pelo SIAD (sininho de notificações). Não requer e-mail dos destinatários.</td></tr></tbody></table>

### **Remetente**

Visível apenas quando o tipo de envio for **E-mail**. Selecione um dos remetentes previamente cadastrados no sistema (menu Remetentes Permitidos). O remetente aparece no formato `Nome <email@dominio.com>`.

Caso não seja selecionado, o sistema utilizará o remetente padrão "siad@prefeitura.sp.gov.br".

{% hint style="info" %}
Somente os Administradores do sistema podem configurar remetentes adicionais. Caso necessário, entrar em contato pelo e-mail siad@prefeitura.sp.gov.br para solicitar esse cadastramento.
{% endhint %}

### **Tipo de destinatário**

Define quem receberá a notificação:

<table><thead><tr><th width="157">Tipo</th><th width="403">Descrição</th><th>Disponível em</th></tr></thead><tbody><tr><td><strong>Usuário</strong></td><td>Selecione um ou mais usuários específicos do sistema.</td><td>E-mail e Sistema</td></tr><tr><td><strong>Equipamento</strong></td><td>Selecione equipamentos — o e-mail institucional do equipamento receberá a mensagem.</td><td>E-mail e Sistema</td></tr><tr><td><strong>E-mails</strong></td><td>Informe endereços de e-mail avulsos (externos ou internos).</td><td>Apenas E-mail</td></tr></tbody></table>

> O tipo "E-mails" não está disponível quando o envio é por Sistema, pois notificações internas exigem um usuário vinculado.

### **Seleção dos destinatários**

O campo se adapta ao tipo escolhido:

* **Usuário**: busca por nome, e-mail ou CPF. Permite selecionar múltiplos.
* **Equipamento**: lista de equipamentos com busca. Somente equipamentos com e-mail cadastrado são listados.
* **E-mails**: campo de tags — digite o endereço e pressione Enter para adicionar. Permite múltiplos.

**Operações**

Define quais eventos disparam esta regra. É possível selecionar múltiplas operações na mesma regra:

<table><thead><tr><th width="214.666748046875">Operação</th><th>Quando é disparada</th></tr></thead><tbody><tr><td><strong>Alteração de status</strong></td><td>Quando o status de um protocolo é alterado (manualmente por um Editor/Administrador).</td></tr><tr><td><strong>Exclusão</strong></td><td>Quando um protocolo é excluído (soft delete).</td></tr><tr><td><strong>Restauração</strong></td><td>Quando um protocolo excluído é restaurado.</td></tr></tbody></table>

### **Assunto**

Visível apenas para envio por **E-mail**. Define a linha de assunto da mensagem.

Suporta variáveis dinâmicas que serão substituídas no momento do envio:

* `{operacao}` — nome da operação realizada (ex: "Alteração de status")
* `{titulo}` — nome do fluxo

Exemplo: `SIAD Forms - {operacao} - {titulo}`

Se deixado em branco, o sistema utilizará um assunto padrão.

### **Conteúdo**

Editor de texto rico para compor o corpo da notificação. Permite formatação com negrito, itálico, listas, links e tabelas.

Se deixado em branco, o sistema enviará uma mensagem padrão com informações do evento.

***

## Exemplos de configuração

### **Exemplo 1 — Notificar coordenação sobre exclusão de protocolos**

<table><thead><tr><th width="212.6666259765625">Campo</th><th>Valor</th></tr></thead><tbody><tr><td>Tipo de envio</td><td>E-mail</td></tr><tr><td>Remetente</td><td>siad@prefeitura.sp.gov.br</td></tr><tr><td>Tipo de destinatário</td><td>Usuário</td></tr><tr><td>Destinatários</td><td>Maria Coordenadora, João Supervisor</td></tr><tr><td>Operações</td><td>Exclusão, Restauração</td></tr><tr><td>Assunto</td><td>SIAD Forms - {operacao} - {titulo}</td></tr><tr><td>Conteúdo</td><td>(em branco — mensagem padrão)</td></tr></tbody></table>

### **Exemplo 2 — Notificação interna para equipe sobre alteração de status**

<table><thead><tr><th width="214">Campo</th><th>Valor</th></tr></thead><tbody><tr><td>Tipo de envio</td><td>Sistema</td></tr><tr><td>Tipo de destinatário</td><td>Equipamento</td></tr><tr><td>Destinatários</td><td>CRAS Centro, CRAS Norte</td></tr><tr><td>Operações</td><td>Alteração de status</td></tr></tbody></table>

### **Exemplo 3 — Alertar e-mails externos sobre qualquer evento**

<table><thead><tr><th width="203.3333740234375">Campo</th><th>Valor</th></tr></thead><tbody><tr><td>Tipo de envio</td><td>E-mail</td></tr><tr><td>Remetente</td><td>siad@prefeitura.sp.gov.br</td></tr><tr><td>Tipo de destinatário</td><td>E-mails</td></tr><tr><td>Destinatários</td><td><a href="mailto:gestor@org.com.br">gestor@org.com.br</a>, <a href="mailto:coordenacao@parceiro.org">coordenacao@parceiro.org</a></td></tr><tr><td>Operações</td><td>Alteração de status, Exclusão, Restauração</td></tr><tr><td>Assunto</td><td>[SIAD] {operacao} no fluxo {titulo}</td></tr><tr><td>Conteúdo</td><td>Informamos que houve uma atualização no protocolo vinculado ao fluxo. Acesse o sistema para mais detalhes.</td></tr></tbody></table>

***

## Múltiplas regras

É possível cadastrar quantas regras forem necessárias. Cada regra é avaliada independentemente — todas as regras cujas operações coincidam com o evento ocorrido terão suas notificações disparadas.

Isso permite, por exemplo:

* Uma regra para notificar a coordenação por e-mail em caso de exclusão
* Outra regra para notificar toda a equipe por sistema em caso de alteração de status
* Outra regra para alertar um parceiro externo por e-mail em qualquer evento

***

## Considerações

* As notificações são disparadas de forma assíncrona (não bloqueiam a ação do usuário).
* O toggle **Habilitar notificações** funciona como um interruptor geral: se desativado, todas as regras ficam suspensas sem necessidade de excluí-las.
* Notificações do fluxo complementam as notificações das etapas — ambas podem coexistir sem conflito.
* Alterações nas regras de notificação têm efeito imediato, independentemente do status do fluxo.
