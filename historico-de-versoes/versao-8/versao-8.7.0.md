# Versão 8.7.0

## Novas Funcionalidades

### Meus Forms

Foi disponibilizada no SIAD Forms uma nova página inicial para o painel de formulários, reunindo em um só lugar as opções de consulta e acompanhamento. Usuários anônimos e logados podem consultar um protocolo informando seu número, enquanto os usuários autenticados também acessam a área “Meus protocolos”, com cartões que exibem o fluxo, o número do protocolo e a próxima etapa, além de busca, ordenação e filtro de protocolos concluídos. A página também apresenta os formulários disponíveis para acesso, com pesquisa e opção de exibir formulários públicos. Ao consultar um protocolo próprio ou de outro solicitante, o sistema informa a origem e direciona o usuário para a etapa correspondente.

## Melhorias

### Novo status "Aguardando deliberação do gabinete"

Foi adicionado um novo status "Aguardando deliberação do gabinete" para projetos indicando que o projeto que depende de uma decisão do gabinete para prosseguir.

### **Descrição dos Objetivos Estratégicos no Planejamento**

Foi disponibilizado no SIAD o cadastro de descrições para os Objetivos Estratégicos e Resultados Chave do planejamento. Agora, além do nome, é possível registrar uma explicação detalhada sobre cada objetivo, exibida na tabela de cadastro com apoio de tooltip. No formulário de projetos, uma nova ação permite consultar, em um painel lateral, o nome e a descrição de todos os objetivos estratégicos antes de realizar a seleção. A melhoria facilita a compreensão dos objetivos e apoia o correto enquadramento dos projetos.

### Página Meus Forms no SIAD Forms

O Meus Forms passou a ser exibido como um módulo na seleção de módulos do SIAD, junto aos demais módulos disponíveis para o vínculo. Ao escolhê-lo, o usuário é levado à página inicial do SIAD Forms. Na tela de login, foi incluído o link "Consultar protocolo e formulários públicos", que permite acessar a consulta sem autenticação. Na página do SIAD Forms, usuários não autenticados contam com o botão "Entrar", e a seção "Meus protocolos" fica sempre visível, bloqueada até o login. Usuários que ainda não aceitaram o termo de uso visualizam o termo antes de acessar o módulo.

## Ajustes

### Correção de redirecionamento no login

No SIAD, foi corrigido o redirecionamento após o login para respeitar o módulo selecionado pelo usuário. Quando o acesso parte de uma página específica de um painel autorizado, o sistema mantém o destino original; já páginas iniciais de painéis, destinos externos ou áreas sem permissão levam ao módulo escolhido.

### Permissões de campos para Editor do fluxo

No SIAD Forms, foi corrigida a aplicação das permissões de acesso dos campos para usuários com perfil Editor no fluxo. Agora esses usuários recebem as permissões configuradas para o perfil Editor, e não as do perfil Usuário, e os campos configurados com permissão de alteração voltam a ser exibidos na edição da resposta.
