# Gerenciar Respostas

## Introdução

A tela de **Respostas** oferece uma visão orientada às respostas individuais das etapas, em contraste com a tela de Protocolos que agrupa tudo por registro. É acessada pelo menu lateral **SIAD Forms > Respostas**.

A principal vantagem dessa tela é que, ao filtrar por fluxo e etapa, as colunas da tabela se expandem para exibir os **atributos configurados com visibilidade na tabela**, permitindo visualizar e pesquisar os dados preenchidos diretamente na listagem, sem necessidade de abrir cada protocolo individualmente.

> **Dica**: para exportação de dados, criação de painéis, indicadores e visualizações analíticas avançadas das respostas, utilize o **Metabase**. O SIAD Forms não oferece funcionalidade nativa de exportação ou dashboards; o Metabase está conectado à base de dados e permite consultas personalizadas, gráficos e relatórios a partir das tabelas de protocolos e respostas.

***

### Colunas fixas

Independentemente dos filtros aplicados, as seguintes colunas são sempre exibidas:

<table><thead><tr><th width="186.6666259765625">Coluna</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Protocolo</strong></td><td>Número do protocolo vinculado à resposta. Pesquisável individualmente.</td></tr><tr><td><strong>Fluxo</strong></td><td>Nome do fluxo ao qual a resposta pertence.</td></tr><tr><td><strong>Equipamento</strong></td><td>Equipamento do usuário que registrou a resposta.</td></tr><tr><td><strong>Etapa</strong></td><td>Nome da etapa em que a resposta foi registrada.</td></tr><tr><td><strong>Registrado</strong></td><td>Data de criação e usuário que cadastrou a resposta.</td></tr><tr><td><strong>Alterado</strong></td><td>Data da última alteração da resposta.</td></tr></tbody></table>

### Colunas dinâmicas (atributos)

Ao filtrar por um **fluxo** e uma **etapa** específica, colunas adicionais aparecem automaticamente na tabela. Essas colunas correspondem aos atributos do formulário da etapa que foram configurados com a opção **"Visibilidade na tabela?"** ativa (veja a documentação de configuração de atributos na seção).

As colunas dinâmicas:

* Exibem o valor preenchido pelo respondente diretamente na célula
* São pesquisáveis individualmente (campo de busca por coluna)
* Formatam automaticamente valores de data e data/hora
* Desaparecem quando o filtro de etapa é removido

Para que um atributo apareça como coluna, ele precisa estar com a flag "Visibilidade na tabela?" ativa na configuração do atributo dentro da seção do formulário vinculado à etapa.

***

### Filtros disponíveis

Os filtros ficam acima da tabela:

<table><thead><tr><th width="198">Filtro</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Fluxo</strong></td><td>Filtra respostas de um fluxo específico. Ao selecionar, o filtro de Etapa é habilitado.</td></tr><tr><td><strong>Etapa</strong></td><td>Filtra respostas de uma etapa específica. Lista apenas etapas da versão publicada (ou que possuam respostas em versões arquivadas) do fluxo selecionado. Exibe o número da versão entre parênteses. <strong>É a seleção deste filtro que ativa as colunas dinâmicas.</strong></td></tr><tr><td><strong>Equipamento</strong></td><td>Filtra respostas pelo equipamento do usuário que as cadastrou. Aceita múltipla seleção.</td></tr><tr><td><strong>Registro excluído</strong></td><td>Permite incluir ou exibir apenas respostas excluídas (soft deleted).</td></tr></tbody></table>

***

### Ação de visualização

Cada linha da tabela possui o botão **Visualizar** (ícone de olho) que redireciona para a tela de visualização do **Protocolo** correspondente, posicionando automaticamente na aba da etapa da resposta clicada.

A partir daí, o comportamento é idêntico ao descrito na página "Gerenciar Protocolos": é possível ver todas as abas do protocolo, editar, excluir, restaurar e imprimir conforme as permissões.

***

### Impressão em lote

Assim como na tela de protocolos, é possível selecionar múltiplas respostas e clicar em **Imprimir selecionados**. A impressão em lote gera uma página unificada com todas as respostas selecionadas.

Restrições:

* Todas as respostas selecionadas devem pertencer ao mesmo fluxo
* O fluxo deve ter a impressão habilitada
* Cada etapa das respostas selecionadas também deve ter a impressão habilitada
* Respostas excluídas não são incluídas

***

### Visibilidade e permissões

A tela de respostas respeita as mesmas regras de acesso da tela de protocolos:

* Apenas respostas de etapas às quais o usuário tem permissão de **Consultar** são listadas
* A restrição de acesso por etapa (usuário/equipamento/temática) é aplicada
* A restrição de acesso ao fluxo (nível de protocolo) também é considerada
* Administradores do Sistema e do Fluxo, bem como Editores, veem todas as respostas sem restrição

***

### Quando usar Respostas vs Protocolos

<table><thead><tr><th width="490">Cenário</th><th>Tela recomendada</th></tr></thead><tbody><tr><td>Preciso ver uma visão geral dos protocolos e seus status</td><td>Protocolos</td></tr><tr><td>Preciso alterar o status ou observações de protocolos</td><td>Protocolos</td></tr><tr><td>Preciso visualizar dados preenchidos de uma etapa específica lado a lado</td><td><strong>Respostas</strong></td></tr><tr><td>Preciso buscar uma resposta por valor de um campo específico</td><td><strong>Respostas</strong></td></tr><tr><td>Preciso imprimir respostas de uma etapa</td><td><strong>Respostas</strong></td></tr><tr><td>Preciso excluir ou restaurar um protocolo inteiro</td><td>Protocolos</td></tr></tbody></table>
