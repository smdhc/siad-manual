# Gerenciar Protocolos

### Introdução

Protocolos são os registros gerados quando respondentes preenchem a etapa inicial de um fluxo. Cada protocolo possui um número único, um status, e agrega todas as respostas dadas nas diferentes etapas ao longo do processo.

Para acessar a gestão de protocolos, navegue até **SIAD Forms > Protocolos** no menu lateral.

***

## Listagem de protocolos

A tela principal exibe todos os protocolos aos quais o usuário tem acesso, ordenados por data de criação (mais recentes primeiro). Protocolos excluídos são destacados com fundo avermelhado.

### **Colunas disponíveis**

<table><thead><tr><th width="219.3333740234375">Coluna</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Nº Protocolo</strong></td><td>Número sequencial único gerado automaticamente. Copiável com um clique.</td></tr><tr><td><strong>Fluxo</strong></td><td>Nome do fluxo ao qual o protocolo pertence.</td></tr><tr><td><strong>Versão</strong></td><td>Número da versão do fluxo em que o protocolo foi criado.</td></tr><tr><td><strong>Equipamento</strong></td><td>Equipamento do usuário que cadastrou o protocolo.</td></tr><tr><td><strong>Status</strong></td><td>Status atual do protocolo (conforme os status configurados no fluxo).</td></tr><tr><td><strong>Observações</strong></td><td>Texto de observações do protocolo (oculto por padrão).</td></tr><tr><td><strong># Etapas Preenchidas</strong></td><td>Quantidade de respostas registradas no protocolo.</td></tr><tr><td><strong>Última Resposta</strong></td><td>Data/hora da resposta mais recente, com o nome da etapa em descrição.</td></tr><tr><td><strong>Registrado</strong></td><td>Data de criação e usuário que cadastrou.</td></tr><tr><td><strong>Alterado</strong></td><td>Data da última alteração (oculto por padrão).</td></tr></tbody></table>

### **Filtros**

Os filtros ficam acima da tabela e permitem refinar a listagem:

<table><thead><tr><th width="194.666748046875">Filtro</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Fluxo</strong></td><td>Filtra protocolos de um fluxo específico. Ao selecionar, os filtros de Versão e Status se atualizam para exibir apenas opções daquele fluxo.</td></tr><tr><td><strong>Versão</strong></td><td>Filtra por versão do fluxo. Disponível apenas quando um fluxo está selecionado.</td></tr><tr><td><strong>Status</strong></td><td>Filtra por um ou mais status. Se nenhum fluxo estiver selecionado, lista os status de todos os fluxos acessíveis (sem duplicidades de nome).</td></tr><tr><td><strong>Equipamento</strong></td><td>Filtra protocolos pelo equipamento do usuário que os cadastrou.</td></tr><tr><td><strong>Registro excluído</strong></td><td>Permite incluir ou exibir apenas protocolos excluídos.</td></tr></tbody></table>

***

## Visualizar um protocolo

Clique no botão de visualização (ícone de olho) na linha do protocolo. A tela de visualização é organizada em abas:

### **Aba "Dados Gerais"**

Exibe informações resumidas do protocolo:

* Número do protocolo (copiável)
* Status atual (em badge colorido)
* Fluxo e versão
* Equipamento e usuário de cadastro
* Data de cadastro
* Observações (se houver)
* Seção de auditoria (expansível) com detalhes de inclusão e alteração

### **Ações disponíveis no cabeçalho:**

* **Atualizar Protocolo**: abre modal para alterar status e observações (visível para Editores e Administradores)
* **Imprimir protocolo**: abre página de impressão em nova aba (visível quando impressão está habilitada no fluxo)

### **Abas de etapas**

Cada etapa do fluxo aparece como uma aba separada, exibindo:

* **Quando há resposta**: os dados preenchidos organizados por seção, com os campos renderizados no formato de leitura. Ações de editar, excluir, imprimir e baixar anexos ficam disponíveis conforme permissões.
* **Quando não há resposta**: mensagem informativa com botão "Preencher Formulário" (link para a URL pública da etapa com o protocolo preenchido) e/ou botão de restauração caso exista resposta excluída.
* **Quando sem permissão**: mensagem "Você não possui permissão para visualizar as respostas desta etapa."

***

## Alterar status e observações

Existem duas formas de alterar status e observações de protocolos:

**Individualmente**

Na tela de visualização do protocolo, clique em **Atualizar Protocolo** no cabeçalho da seção "Protocolo". O modal exibe:

<table><thead><tr><th width="192">Campo</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Status</strong></td><td>Selecione o novo status entre os status configurados no fluxo.</td></tr><tr><td><strong>Observações</strong></td><td>Texto livre para registrar informações sobre o protocolo.</td></tr></tbody></table>

**Em lote**

Na listagem de protocolos, selecione múltiplos protocolos usando os checkboxes e clique em **Atualizar Status/Observações** na barra de ações em massa. O mesmo modal é exibido e as alterações são aplicadas a todos os protocolos selecionados.

> **Quem pode alterar**: Administradores do Sistema, Administradores do Fluxo e Editores do Fluxo.

***

## Consultar respostas por etapa

Na tela de visualização do protocolo, navegue pelas abas para ver as respostas de cada etapa. Cada aba exibe:

* Os dados preenchidos organizados por seção do formulário
* Versão do formulário utilizada na resposta
* Dados de auditoria (quem cadastrou, quando, quem alterou)

As respostas são exibidas respeitando:

* Regras de visibilidade de atributos (campos ocultados por configuração de acesso não aparecem)
* Restrição de visualização por etapa (se configurada)
* Condicionais de campos dependentes (campos vinculados a campo pai que não satisfazem a condição não aparecem, exceto se possuem valor preenchido — preservação de histórico)

***

## Ações sobre respostas individuais

Dentro de cada aba de etapa, as seguintes ações podem estar disponíveis:

<table><thead><tr><th width="228.3333740234375">Ação</th><th>Condições</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Editar Dados</strong></td><td>Edição habilitada na etapa + permissão de Alterar + status permitido + dentro do prazo</td><td>Abre o formulário em modo de edição na URL pública.</td></tr><tr><td><strong>Excluir Resposta</strong></td><td>Exclusão habilitada na etapa + permissão de Excluir + status permitido + dentro do prazo</td><td>Exclui a resposta (soft delete). Se já existem respostas excluídas anteriores, estas são removidas permanentemente.</td></tr><tr><td><strong>Restaurar Resposta</strong></td><td>Permissão de Reativar ou Administrador + existe resposta excluída</td><td>Restaura a resposta excluída mais recente.</td></tr><tr><td><strong>Imprimir resposta</strong></td><td>Impressão habilitada no fluxo e na etapa</td><td>Abre página de impressão individual da resposta.</td></tr><tr><td><strong>Baixar todos os anexos (ZIP)</strong></td><td>Etapa possui campos de arquivo com valores preenchidos</td><td>Faz download de todos os arquivos anexados naquela etapa em um arquivo ZIP.</td></tr><tr><td><strong>Preencher Formulário</strong></td><td>Etapa sem resposta + permissão de Cadastrar + dentro do prazo</td><td>Link para a URL pública da etapa com o número de protocolo preenchido.</td></tr><tr><td><strong>Atualizar dados</strong></td><td>Permissão de Alterar (após editar via URL externa)</td><td>Recarrega a página para refletir alterações feitas em outra aba.</td></tr></tbody></table>

***

## Excluir e restaurar protocolos

### **Excluir protocolo**

* Disponível apenas para **Administradores do Sistema** e **Administradores do Fluxo**.
* Editores do fluxo **não** podem excluir protocolos.
* A exclusão é reversível (soft delete) — o protocolo fica com fundo avermelhado na listagem.
* Pode ser feita individualmente (botão na tela de visualização) ou em lote (selecionando múltiplos na listagem).

### **Restaurar protocolo**

* Disponível apenas para **Administradores do Sistema** e **Administradores do Fluxo**.
* Na tela de visualização de um protocolo excluído, o botão **Restaurar** fica disponível no cabeçalho.
* A restauração reverte o soft delete e o protocolo volta ao estado normal.

***

## Impressão

O SIAD Forms oferece duas modalidades de impressão:

### **Impressão do protocolo completo**

Gera uma página formatada com todos os dados do protocolo e respostas de todas as etapas. Disponível quando a opção "Habilitar impressão do protocolo" está ativa nos Dados Gerais do fluxo.

Acesso:

* Botão **Imprimir protocolo** no cabeçalho da visualização
* Botão **Imprimir protocolo** no topo das páginas públicas (modo consulta)

### **Impressão individual por etapa**

Gera uma página formatada apenas com os dados da resposta de uma etapa específica. Disponível quando a impressão está habilitada tanto no fluxo quanto na etapa.

Acesso:

* Botão **Imprimir resposta** dentro da aba da etapa (painel interno)
* Botão **Imprimir resposta** na tela pública de acompanhamento

### **Impressão em lote**

Na listagem de protocolos, selecione múltiplos protocolos e clique em **Imprimir selecionados**. Gera uma página de impressão unificada com todos os protocolos selecionados.

Restrições:

* Todos os protocolos selecionados devem pertencer ao mesmo fluxo
* O fluxo deve ter a impressão habilitada
* Protocolos excluídos não são incluídos

***

## Visibilidade dos protocolos

A listagem de protocolos respeita múltiplas camadas de controle de acesso:

1. **Administradores do Sistema**: veem todos os protocolos de todos os fluxos.
2. **Administradores e Editores do Fluxo**: veem todos os protocolos do fluxo, sem restrição.
3. **Usuários com permissão em etapas**: veem protocolos que possuem respostas em etapas às quais têm acesso de consulta, ou que pertencem a versões com etapas acessíveis.
4. **Restrição de acesso ao fluxo** (se configurada): filtra ainda mais, exibindo apenas protocolos cadastrados pelo próprio usuário, pelo mesmo equipamento ou pela mesma temática, conforme a regra configurada.

Essa camada dupla (permissão na etapa + restrição no fluxo) garante que cada usuário visualize apenas os protocolos relevantes para sua atuação.
