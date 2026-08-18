# Versão 8.5.0

## Funcionalidade de cadastrar Turmas para lançamentos facilitados de Atividades Coletivas

Ao cadastrar uma Turma de participantes recorrentes de uma determinada Atividade Coletiva, os usuários poderão registrar atividades de maneira simplificada, sem necessitar buscar e selecionar munícipe por munícipe.

## Correção da URL de Redefinição de Senha

Ajustamos a URL da tela de redefinição de senha para manter o padrão e a organização das rotas de autenticação da aplicação. A rota antiga `/atendimento/pasword-reset` foi corrigida e agora o acesso ocorre adequadamente através do caminho `/auth/password-reset`.

## Novo Botão no E-mail de Redefinição de Senha

Melhoramos a experiência e o visual das nossas comunicações de recuperação de conta. Além do link em formato de texto simples doi adicionado um botão em HTML estilizado, tornando a ação de redefinir a senha muito mais clara e intuitiva para o usuário.

## Preenchimento Automático do Nome de Passkeys

Facilitamos o processo de registro e gerenciamento de dispositivos de segurança. Agora, o sistema identifica e preenche automaticamente o nome da Passkey utilizando o AAGUID (Authenticator Attestation Global Unique Identifier) do dispositivo, poupando tempo na configuração.

## Modal de Incentivo para Criação de Passkeys

Para incentivar o uso de métodos de autenticação mais modernos e seguros, implementamos um novo modal na plataforma. Usuários que acessam o sistema e ainda não possuem uma Passkey vinculada à conta receberão um aviso amigável logo após o login, convidando-os a configurar essa nova credencial

## Criação de Perfis de Impressão no SIAD Forms

Agora é possível criar "perfis de impressão" personalizados nas configurações de cada etapa do SIAD Forms. Ao ativar a opção "Permitir impressão da resposta", um novo menu de repetição será exibido logo abaixo, permitindo nomear o perfil e selecionar exatamente quais campos devem constar no documento. No momento da impressão, o usuário poderá escolher qual dos perfis criados deseja utilizar, além de ter sempre à disposição a opção padrão de "imprimir tudo", que não exige configuração prévia.

## Mensagem de Sucesso Customizável no SIAD Forms

Agora é possível definir uma mensagem de sucesso personalizada para ser exibida ao usuário logo após o envio de uma resposta no SIAD Forms. Essa configuração pode ser realizada de forma simples diretamente na aba "Identificação" durante a edição de uma etapa. Com essa novidade, você pode substituir o texto padrão do sistema por instruções específicas, agradecimentos ou próximos passos, garantindo uma comunicação muito mais clara e alinhada com o propósito do seu formulário.

## Botão de Consulta de Protocolo no SIAD Forms

Para facilitar o acompanhamento e a gestão das solicitações, foi adicionado um novo botão de "Consultar protocolo" diretamente na tela de sucesso do SIAD Forms. Assim que o usuário finaliza e envia a sua resposta, este botão fica imediatamente disponível, permitindo o acesso rápido aos dados do protocolo gerado. Isso elimina a necessidade de navegação extra, oferecendo uma experiência mais ágil e transparente para quem acabou de preencher o formulário.

## Melhorias de Depuração no Laravel Pulse

O painel de monitoramento do sistema recebeu melhorias significativas em suas ferramentas de depuração com a atualização do Laravel Pulse. Agora, o dashboard principal exibe informações muito mais detalhadas e aprofundadas sobre o desempenho e os processos em execução. Essa evolução permite que administradores e desenvolvedores monitorem a saúde da aplicação, identifiquem gargalos e analisem métricas com maior precisão e rapidez, tudo centralizado em uma única interface.
