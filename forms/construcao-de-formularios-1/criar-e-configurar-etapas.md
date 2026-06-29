# Criar e Configurar Etapas

## Introdução

As etapas são o coração do fluxo — cada uma representa um momento de coleta de dados, com seu próprio formulário, regras de acesso e comportamento. Para gerenciar as etapas, acesse a versão desejada do fluxo e clique no botão **Etapas** (ou acesse via sub-navegação).

A tela de etapas exibe no topo o nome do fluxo, o número da versão e seu status atual. Somente versões com status **Rascunho** permitem criar novas etapas.

Para criar uma etapa, clique em **Cadastrar Etapa**. O formulário é organizado em abas:

***

## Aba Identificação

Define os dados essenciais da etapa: quem ela é, como será acessada e qual formulário será utilizado.

<table><thead><tr><th width="189.6666259765625">Campo</th><th width="143.6666259765625" align="center">Obrigatório</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Nome da Etapa</strong></td><td align="center">Sim</td><td>Nome de identificação interna. Será exibido nas abas de acompanhamento e na listagem de etapas. Ex: "Inscrição", "Análise Técnica", "Devolutiva".</td></tr><tr><td><strong>Título</strong></td><td align="center">Não</td><td>Título exibido ao respondente no topo do formulário. Se não preenchido, será usado o Nome da Etapa.</td></tr><tr><td><strong>Subtítulo</strong></td><td align="center">Não</td><td>Texto complementar exibido abaixo do título. Útil para instruções curtas ou informações de contexto.</td></tr><tr><td><strong>Ordem de exibição</strong></td><td align="center">Não</td><td>Número que define a posição da etapa nas abas de acompanhamento do protocolo. Menor número = mais à esquerda.</td></tr><tr><td><strong>Tipo</strong></td><td align="center">Sim</td><td>Define o comportamento da etapa (veja detalhes abaixo). Não pode ser alterado após criação.</td></tr><tr><td><strong>Visibilidade</strong></td><td align="center">Sim</td><td>Define quem pode acessar a etapa (veja detalhes abaixo).</td></tr><tr><td><strong>Formulário vinculado</strong></td><td align="center">Sim</td><td>Selecione o formulário cujos campos serão utilizados nesta etapa. Somente formulários que possuam pelo menos uma versão publicada são listados. Não pode ser alterado após criação.</td></tr><tr><td><strong>Versão do formulário</strong></td><td align="center">Sim</td><td>Selecione a versão publicada do formulário. Pode ser atualizada posteriormente para apontar para versões mais recentes.</td></tr><tr><td><strong>Slug (URL pública)</strong></td><td align="center">Condicional</td><td>Identificador único usado na URL de acesso público (<code>/forms/{slug}</code>). Obrigatório para etapas com visibilidade Público. Formato: letras minúsculas, números e hífens. Ex: <code>inscricao-programa-2026</code>.</td></tr><tr><td><strong>Banner</strong></td><td align="center">Não</td><td>Imagem exibida no topo do formulário público. Upload de arquivo ou imagem já armazenada.</td></tr><tr><td><strong>Banner hook</strong></td><td align="center">Não</td><td>Define a posição de renderização do banner na página. Padrão: início do conteúdo.</td></tr><tr><td><strong>Alinhamento do banner</strong></td><td align="center">Não</td><td>Define o alinhamento horizontal do banner: Esquerda, Centro, Direita ou Largura Total (padrão).</td></tr><tr><td><strong>Cor de fundo da página</strong></td><td align="center">Não</td><td>Permite personalizar a cor de fundo da página pública do formulário.</td></tr></tbody></table>

### **Tipo de Etapa**

<table><thead><tr><th width="196">Tipo</th><th>Comportamento</th></tr></thead><tbody><tr><td><strong>Inicial</strong></td><td>Ao ser respondida, gera um <strong>novo protocolo</strong> com número sequencial. É o ponto de entrada do fluxo. Cada fluxo deve ter pelo menos uma etapa inicial.</td></tr><tr><td><strong>Intermediária</strong></td><td>Exige que o respondente informe um número de protocolo existente para acessá-la. Permite dar continuidade ao processo já iniciado.</td></tr></tbody></table>

### **Visibilidade**

<table><thead><tr><th width="144">Visibilidade</th><th>Comportamento</th></tr></thead><tbody><tr><td><strong>Público</strong></td><td>Qualquer pessoa pode acessar o formulário pela URL <code>/forms/{slug}</code>, sem necessidade de login.</td></tr><tr><td><strong>Interno</strong></td><td>Somente usuários logados com permissão configurada na aba de Permissões podem acessar.</td></tr></tbody></table>

***

## Aba Regras de Fluxo

Configura quando e sob quais condições a etapa fica disponível, e qual o efeito de respondê-la sobre o protocolo.

<table><thead><tr><th width="204">Campo</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Pré-requisito de status</strong></td><td>Visível apenas para etapas intermediárias. Define quais status o protocolo deve ter para que esta etapa seja liberada. Se o protocolo não estiver em nenhum dos status selecionados, o acesso é bloqueado. Se vazio, a etapa é acessível independentemente do status.</td></tr><tr><td><strong>Status atribuído ao responder</strong></td><td>Define qual status o protocolo receberá automaticamente quando uma resposta for registrada nesta etapa. Útil para automatizar a progressão (ex: ao responder "Análise", o protocolo muda para "Analisado"). Se vazio, o status não é alterado.</td></tr><tr><td><strong>Disponível a partir de</strong></td><td>Data/hora a partir da qual o formulário pode ser preenchido. Antes desse momento, o formulário é exibido como indisponível.</td></tr><tr><td><strong>Disponível até</strong></td><td>Data/hora limite para preenchimento. Após esse momento, novas respostas não são aceitas, mas respostas existentes podem ser consultadas.</td></tr><tr><td><strong>Permitir acompanhamento pelo link público</strong></td><td>Quando ativado, permite que o respondente consulte a resposta gravada informando o número do protocolo na mesma URL da etapa. Habilita o botão "Consultar Protocolo" no formulário.</td></tr></tbody></table>

### **Como funciona o pré-requisito de status**

Exemplo prático para um fluxo com 3 etapas:

1. **Inscrição** (inicial) → ao responder, protocolo recebe status "Pendente"
2. **Análise** (intermediária, pré-requisito: "Pendente") → ao responder, protocolo recebe status "Analisado"
3. **Devolutiva** (intermediária, pré-requisito: "Analisado") → ao responder, protocolo recebe status "Concluído"

Neste cenário, a etapa "Análise" só é acessível enquanto o protocolo estiver com status "Pendente", e a "Devolutiva" só após a análise ser concluída.

***

## Aba Respostas

Controla o que pode ser feito com as respostas já registradas nesta etapa.

<table><thead><tr><th width="240.6666259765625">Campo</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Permitir edição de respostas</strong></td><td>Quando ativado, habilita o botão "Editar Dados" na tela de consulta do protocolo para usuários com permissão de Alterar.</td></tr><tr><td><strong>Edição permitida nos status</strong></td><td>Visível quando edição está habilitada. Define em quais status do protocolo a edição é possível. Se vazio, a edição é permitida em qualquer status.</td></tr><tr><td><strong>Permitir exclusão de respostas</strong></td><td>Quando ativado, habilita o botão "Excluir Resposta" para usuários com permissão de Excluir. A exclusão é reversível (soft delete).</td></tr><tr><td><strong>Exclusão permitida nos status</strong></td><td>Visível quando exclusão está habilitada. Define em quais status do protocolo a exclusão é possível.</td></tr><tr><td><strong>Restringir visualização das respostas</strong></td><td>Controla quem pode ver as respostas desta etapa. Não afeta Administradores e Editores do fluxo. Opções:</td></tr><tr><td></td><td>- <em>Usuário</em>: somente quem cadastrou a resposta pode vê-la</td></tr><tr><td></td><td>- <em>Equipamento</em>: somente usuários do mesmo equipamento do cadastrante</td></tr><tr><td></td><td>- <em>Temática</em>: somente usuários da mesma temática</td></tr><tr><td></td><td>Se vazio, todos com permissão de consulta na etapa podem ver.</td></tr><tr><td><strong>Permitir impressão da resposta</strong></td><td>Habilita o botão de impressão individual da resposta desta etapa na tela de acompanhamento. A impressão geral do fluxo também precisa estar habilitada (nos Dados Gerais do fluxo).</td></tr><tr><td><strong>Ocultar aba no acompanhamento quando sem resposta</strong></td><td>Quando ativado, a aba desta etapa não é exibida na tela de acompanhamento se não houver resposta cadastrada <strong>e</strong> o status atual do protocolo não for o pré-requisito configurado. Se o status do protocolo corresponder ao pré-requisito, a aba permanece visível (indicando que a etapa está aguardando preenchimento).</td></tr></tbody></table>

### **Diferença entre restrição do Fluxo e da Etapa**

<table><thead><tr><th width="173.6666259765625"></th><th>Restrição do Fluxo</th><th>Restrição da Etapa</th></tr></thead><tbody><tr><td><strong>Escopo</strong></td><td>Protocolo inteiro</td><td>Resposta de uma etapa específica</td></tr><tr><td><strong>Efeito</strong></td><td>Protocolo não aparece na listagem</td><td>Protocolo aparece, mas a resposta da etapa fica oculta</td></tr><tr><td><strong>Base</strong></td><td>Quem cadastrou o protocolo</td><td>Quem cadastrou a resposta da etapa</td></tr><tr><td><strong>Configuração</strong></td><td>Dados Gerais do Fluxo</td><td>Aba Respostas da Etapa</td></tr></tbody></table>

***

## Aba Permissões de Acesso

Define quem pode acessar e interagir com esta etapa. Clique em **Adicionar nova permissão** para incluir regras.

Cada regra é composta por:

### **Tipo de entidade**

<table><thead><tr><th width="210">Tipo</th><th>Comportamento</th></tr></thead><tbody><tr><td><strong>Usuário</strong></td><td>Acesso concedido a usuários específicos (busca por nome, e-mail ou CPF).</td></tr><tr><td><strong>Equipamento</strong></td><td>Acesso concedido a todos os usuários dos equipamentos selecionados.</td></tr><tr><td><strong>Temática</strong></td><td>Acesso concedido a todos os usuários de equipamentos das temáticas selecionadas.</td></tr><tr><td><strong>Tipo de Equipamento</strong></td><td>Acesso concedido a todos os usuários de equipamentos dos tipos selecionados.</td></tr><tr><td><strong>Protocolo</strong></td><td>Acesso concedido apenas para protocolos específicos (busca pelo número do protocolo).</td></tr><tr><td><strong>Qualquer usuário</strong></td><td>Concede o acesso a qualquer usuário logado, sem restrição de entidade.</td></tr></tbody></table>

### **Tipo de acesso**

Para cada regra, selecione uma ou mais ações permitidas:

<table><thead><tr><th width="176.666748046875">Ação</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Consultar</strong></td><td>Visualizar respostas gravadas na etapa.</td></tr><tr><td><strong>Cadastrar</strong></td><td>Preencher novas respostas na etapa.</td></tr><tr><td><strong>Alterar</strong></td><td>Editar respostas existentes (requer "Permitir edição" habilitado na aba Respostas).</td></tr><tr><td><strong>Excluir</strong></td><td>Excluir respostas existentes (requer "Permitir exclusão" habilitado na aba Respostas).</td></tr><tr><td><strong>Reativar</strong></td><td>Restaurar respostas excluídas.</td></tr></tbody></table>

### **Regras importantes**

* **Etapas com visibilidade Público**: qualquer pessoa (inclusive sem login) pode cadastrar. As permissões aqui se aplicam às demais ações (consultar, alterar, excluir, reativar).
* **Etapas com visibilidade Interno**: o acesso de cadastro depende obrigatoriamente de uma regra configurada aqui.
* **Administradores do Sistema e do Fluxo**: possuem acesso irrestrito a todas as etapas, independentemente dessas configurações.
* **Múltiplas regras**: são avaliadas de forma independente — o usuário precisa satisfazer pelo menos uma.

### **Configurações adicionais**

<table><thead><tr><th width="221.3333740234375">Campo</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Ocultar aba no acompanhamento quando sem permissão</strong></td><td>Quando ativado, a aba desta etapa fica invisível para usuários sem permissão de consulta. Quando desativado, a aba aparece com a mensagem "Você não possui permissão para visualizar as respostas desta etapa."</td></tr><tr><td><strong>Sincronizar com outras versões</strong></td><td>Visível apenas quando o fluxo possui mais de uma versão. Ao ativar, as configurações de acesso são salvas também para a mesma etapa (identificada pelo UUID) em outras versões do fluxo, evitando reconfiguração manual.</td></tr></tbody></table>

### **Exemplo prático**

Um fluxo de "Acompanhamento de Benefício" com 3 etapas:

<table><thead><tr><th width="206">Etapa</th><th>Regra de acesso</th></tr></thead><tbody><tr><td>Inscrição (público)</td><td>Qualquer pessoa pode cadastrar (público). Equipamento CRAS Centro: Consultar, Alterar.</td></tr><tr><td>Análise (interno)</td><td>Equipamento CRAS Centro: Cadastrar, Consultar. Temática Assistência Social: Consultar.</td></tr><tr><td>Devolutiva (público)</td><td>Qualquer pessoa pode cadastrar (público). Qualquer usuário: Consultar.</td></tr></tbody></table>

## Aba Notificações da Etapa

Configura notificações automáticas específicas para eventos que ocorrem **nesta etapa**. Funciona de forma independente e complementar às notificações do fluxo.

### **Habilitar**

Ative o toggle **Habilitar notificações** para permitir a criação de regras.

### **Anatomia de uma regra**

Cada regra de notificação contém:

<table><thead><tr><th width="196">Campo</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Tipo de envio</strong></td><td><em>E-mail</em> ou <em>Sistema</em> (notificação interna do SIAD).</td></tr><tr><td><strong>Tipo de destinatário</strong></td><td>Quem receberá: <em>Usuário</em>, <em>Equipamento</em>, <em>E-mails</em> (avulsos) ou <em>Atributos</em> (endereços extraídos dos campos preenchidos).</td></tr><tr><td><strong>Destinatários</strong></td><td>Seleção de acordo com o tipo escolhido.</td></tr><tr><td><strong>Operações</strong></td><td>Eventos que disparam a notificação. As opções variam em relação às do fluxo — aqui focam em operações de resposta.</td></tr><tr><td><strong>Assunto</strong></td><td>Linha de assunto do e-mail. Suporta variáveis dinâmicas.</td></tr><tr><td><strong>Conteúdo</strong></td><td>Corpo da notificação com editor de texto rico.</td></tr></tbody></table>

### **Tipo de destinatário "Atributos"**

Exclusivo das notificações de etapa. Permite que o destinatário da notificação seja extraído dinamicamente de um campo preenchido na resposta. Exemplo: se o formulário possui um campo de e-mail do beneficiário, a notificação pode ser enviada automaticamente para o e-mail informado pelo próprio respondente.

### **Diferença entre notificações do Fluxo e da Etapa**

<table><thead><tr><th width="183"></th><th>Notificações do Fluxo</th><th>Notificações da Etapa</th></tr></thead><tbody><tr><td><strong>Gatilho</strong></td><td>Eventos no protocolo (alteração de status, exclusão, restauração)</td><td>Eventos na resposta da etapa (cadastro, edição, exclusão)</td></tr><tr><td><strong>Escopo</strong></td><td>Afeta todos os protocolos do fluxo</td><td>Afeta apenas respostas desta etapa específica</td></tr><tr><td><strong>Destinatário "Atributos"</strong></td><td>Não disponível</td><td>Disponível (extrai e-mail dos campos preenchidos)</td></tr></tbody></table>

***

## Ações disponíveis na listagem de etapas

Após criar as etapas, a listagem oferece as seguintes ações por linha:

<table><thead><tr><th width="206.6666259765625">Ação</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Editar</strong></td><td>Abre o formulário completo da etapa para ajustes (todas as abas).</td></tr><tr><td><strong>Configurar Formulário</strong></td><td>Abre em nova aba a tela de configuração de seções e atributos do formulário vinculado.</td></tr><tr><td><strong>Ver Prévia</strong></td><td>Abre em nova aba uma visualização prévia do formulário sem persistência de dados.</td></tr><tr><td><strong>Ir para o formulário</strong></td><td>Abre em nova aba a URL pública real do formulário (visível apenas quando o fluxo e a versão estão publicados e o slug está configurado).</td></tr><tr><td><strong>Excluir</strong></td><td>Remove a etapa (apenas em versões com status Rascunho).</td></tr></tbody></table>

***

## Publicar a versão diretamente da tela de etapas

Quando todas as etapas estiverem configuradas, é possível publicar a versão diretamente pela tela de etapas, clicando no botão **Publicar** no topo da listagem. Ao confirmar, a versão passa para status "Publicada" e outras versões publicadas são automaticamente arquivadas.

Este botão só aparece quando:

* A versão está em status Rascunho
* O usuário tem permissão para editar a versão
