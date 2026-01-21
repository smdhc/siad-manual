---
description: 'Data de lançamento: a definir'
---

# Versão 6.4.0

A **versão 6.4.0** do SIAD é uma versão que traz melhorias e ajustes diversos.

Confira abaixo todos os detalhes dessa atualização.

## Novas funcionalidades

### Atendimentos - Formulários Externos Dinâmicos

Foi implementada uma nova funcionalidade na tela de configuração dos Tipos de Atendimento, que permite a configuração dinâmica de formulários externos integrados ao registro de atendimento do SIAD. Esses formulários poderão ser utilizados em eventos específicos, como o Carnaval e a Virada Cultural, entre outros.

Mudanças implementadas na funcionalidade Tipo de Atendimento:

* Novo tipo de Visibilidade "Externo";
* Nova seção "Configurações do Formulário" vinculada à visibilidade "Externo";
* Páginas externas (com prefixo "/public/") geradas dinamicamente a partir dessas configurações;
* Número de colunas do formulário de atendimento passa a ser configurável;
* Nova função de duplicação de Tipos de Atendimentos;
* Nova configuração de atributo que permite somar seu respectivo valor à quantidade total do atendimento.

### Projetos - Monitoramento de indicadores

Foi criada uma nova tela para cadastro de Indicadores, acessível tanto pelo menu principal quanto pelo projeto.&#x20;

Além disso, foram adicionados novos campos no cadastro de resultados-chave, permitindo a configuração de indicadores relacionados.

Os projetos passam a aceitar também múltiplos objetivo estratégicos/resultados-chave.

## Melhorias

### Atendimentos - Melhorias e ajustes diversos

* Foi disponibilizado um novo filtro "Termo de busca" que permite realizar buscas por termos específicos dentro do conteúdo dos atendimentos.
* Adicionada nova configuração (administradores) que permite ordenar e pesquisar listas nos formulários de atendimento.

### Cadastro de Pessoas - Revisão da impressão

A impressão da Ficha de Cadastro da Pessoa foi revisada para ocupar menos espaço na folha e para seguir o padrão adotado nos demais impressos.

### Cadastro de Pessoas - Permissão de campos obrigatórios

Foi criada uma nova permissão para Administradores que possibilita a edição de cadastros sem os campos obrigatórios.

### Encaminhamentos - Melhorias e ajustes diversos

Foram realizados os seguintes ajustes e melhorias no módulo de Encaminhamentos:

* Os campos de profissionais do registro de encaminhamento foram substituídos por uma listagem dos profissionais cadastrados no equipamento, permitindo a seleção de múltiplos profissionais. Esse função está disponível somente para novos encaminhamentos. Os encaminhamentos antigos continuarão exibindo os campos antigos.
* Foi adicionada uma nova opção que permite habilitar ou desabilitar as assinaturas no encaminhamento impresso.
* Foi adicionado um novo filtro de profissionais na tela de listagem de encaminhamentos, funcionando somente para novos encaminhamentos nesse novo formato.
* O campo "Endereço da instituição" (nos casos externos) foi ampliado, passando a aceitar um conteúdo maior, se necessário.
* Corrigida a cor padrão do conteúdo do encaminhamento na impressão.
* Foram removidas as linhas separatórias no impresso.
* Foi disponibilizado um novo filtro "Termo de busca" que permite realizar buscas por termos específicos dentro do conteúdo dos encaminhamentos.
* O rol de opções de cores do conteúdo foi simplificado.

### Usuários / Profissionais - Ocupação obrigatória

O campo "Ocupação" passa a ser obrigatório no cadastro de usuários.
