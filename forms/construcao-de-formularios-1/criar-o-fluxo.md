# Criar o fluxo

## Introdução

Para criar um novo fluxo, acesse o menu lateral **SIAD Forms > Fluxos** e clique no botão **Criar** no canto superior direito.

O formulário de criação está dividido em três seções: Dados Gerais, Configurações de Acesso e Notificações.

## Dados Gerais

<table><thead><tr><th width="161">Campo</th><th width="97.666748046875" align="center">Obrigatório</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Nome</strong></td><td align="center">Sim</td><td>Nome identificador do fluxo. Será exibido nas listagens e na navegação interna. Ex: "Inscrição Programa Transcidadania 2026".</td></tr><tr><td><strong>Status</strong></td><td align="center">Sim</td><td>Define a disponibilidade do fluxo. Ao criar, o padrão é <strong>Rascunho</strong>. Somente fluxos com status <strong>Publicado</strong> ficam acessíveis aos respondentes.</td></tr><tr><td><strong>Restringir acesso aos protocolos</strong></td><td align="center">Não</td><td>Controla quem pode visualizar os protocolos gerados neste fluxo. Não se aplica a Administradores e Editores. Opções:</td></tr><tr><td></td><td align="center"></td><td>- <em>Usuário</em>: somente quem cadastrou o protocolo pode vê-lo</td></tr><tr><td></td><td align="center"></td><td>- <em>Equipamento</em>: somente usuários do mesmo equipamento do cadastrante</td></tr><tr><td></td><td align="center"></td><td>- <em>Temática</em>: somente usuários de equipamentos da mesma temática do cadastrante</td></tr><tr><td></td><td align="center"></td><td>Se deixado em branco, todos os usuários com permissão na etapa podem visualizar os protocolos.</td></tr><tr><td><strong>Habilitar impressão do protocolo</strong></td><td align="center">Não</td><td>Quando ativado, exibe botões de impressão na tela de acompanhamento do protocolo e das respostas individuais de cada etapa.</td></tr><tr><td><strong>Status permitidos para as respostas</strong></td><td align="center">Não</td><td>Lista de status que os protocolos deste fluxo poderão assumir. Esses status são usados para controlar a progressão entre etapas e a visualização na listagem. Ex: "Aberto", "Em análise", "Aprovado", "Indeferido".</td></tr><tr><td><strong>Descrição</strong></td><td align="center">Não</td><td>Texto livre para documentar o objetivo do fluxo. Visível apenas internamente.</td></tr></tbody></table>

## **Sobre os status permitidos**

Os status são fundamentais para o funcionamento do fluxo. Eles permitem:

* Indicar em que momento do processo cada protocolo se encontra
* Configurar pré-requisitos nas etapas (ex: "a etapa Análise só é liberada quando o status for Aguardando análise")
* Definir em quais status a edição ou exclusão de respostas é permitida
* Atribuir automaticamente um status ao protocolo quando uma etapa é respondida

Para adicionar um status, clique em **Adicionar Status**, informe o nome e pressione Enter. É possível adicionar quantos status forem necessários e reordená-los depois.

> **Atenção**: caso apague algum status já utilizado em algum protocolo, este passará a ficar sem status vinculado. Altere os status de protocolos existentes antes de modificá-los.

***

## Configurações de Acesso

Esta seção define quem terá permissão para administrar ou editar o fluxo. Essas configurações podem ser ajustadas a qualquer momento após a criação.

Clique em **Adicionar nova permissão** para incluir uma regra. Cada regra é composta por:

<table><thead><tr><th width="172.666748046875">Campo</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Tipo</strong></td><td>Define a entidade que receberá o acesso. Opções: Usuário, Equipamento, Temática, Tipo de Equipamento.</td></tr><tr><td><strong>Entidade</strong></td><td>Selecione um ou mais registros do tipo escolhido. O campo se adapta à seleção anterior (exibe busca de usuários, lista de equipamentos etc.).</td></tr><tr><td><strong>Tipo de Acesso</strong></td><td>Define o nível de permissão concedido. Opções:</td></tr><tr><td></td><td>- <em>Administrador</em>: gerencia etapas, versões e configurações do fluxo. Pode excluir e restaurar protocolos.</td></tr><tr><td></td><td>- <em>Editor</em>: gerencia status e observações dos protocolos. Não pode excluir protocolos.</td></tr></tbody></table>

É possível adicionar múltiplas regras para combinar diferentes entidades e tipos de acesso. Por exemplo:

* Uma regra dando acesso de Administrador a 2 usuários específicos
* Outra regra dando acesso de Editor a todos os usuários de um determinado equipamento

***

## Notificações

Permite configurar notificações automáticas que serão disparadas quando determinados eventos ocorrerem nos protocolos do fluxo (alteração de status, exclusão ou restauração).

<table><thead><tr><th width="216">Campo</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Habilitar notificações</strong></td><td>Toggle que ativa ou desativa o sistema de notificações do fluxo.</td></tr></tbody></table>

Ao ativar, o botão **Adicionar regra** ficará disponível. Cada regra de notificação contém:

<table><thead><tr><th width="183.3333740234375">Campo</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Tipo de envio</strong></td><td>Como a notificação será entregue: <em>E-mail</em> ou <em>Sistema</em> (notificação interna do SIAD).</td></tr><tr><td><strong>Remetente</strong></td><td>Visível apenas para envio por e-mail. Selecione o remetente configurado previamente no sistema.</td></tr><tr><td><strong>Tipo de destinatário</strong></td><td>Quem receberá a notificação: <em>Usuário</em>, <em>Equipamento</em> ou <em>E-mails</em> (endereços avulsos).</td></tr><tr><td><strong>Destinatários</strong></td><td>Campo que se adapta ao tipo selecionado: busca de usuários, seleção de equipamentos ou campo de tags para informar e-mails.</td></tr><tr><td><strong>Operações</strong></td><td>Quais eventos disparam esta notificação. Opções: <em>Alteração de status</em>, <em>Exclusão</em>, <em>Restauração</em>. É possível selecionar múltiplas.</td></tr><tr><td><strong>Assunto</strong></td><td>Assunto do e-mail (apenas para envio por e-mail). Suporta variáveis como <code>{operacao}</code> e <code>{titulo}</code>.</td></tr><tr><td><strong>Conteúdo</strong></td><td>Corpo da notificação com editor de texto rico. Permite formatar o conteúdo com negrito, listas, links etc.</td></tr></tbody></table>

> **Nota**: as notificações configuradas aqui se aplicam a eventos no nível do protocolo (alteração de status, exclusão/restauração do protocolo). Para notificações específicas de respostas em etapas, configure-as diretamente na etapa.

***

## Após criar o fluxo

Ao clicar em **Criar**, o fluxo será salvo e você será redirecionado para a tela de visualização. A partir desse ponto, os próximos passos são:

1. Criar a primeira **versão** do fluxo
2. Dentro da versão, criar as **etapas** com seus formulários vinculados
3. Publicar a versão e, quando tudo estiver pronto, alterar o status do fluxo para **Publicado**
