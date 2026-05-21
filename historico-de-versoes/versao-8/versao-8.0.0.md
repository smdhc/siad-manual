---
description: 'Data de lançamento: a definir'
---

# Versão 8.0.0

A **versão 8.0.0** do SIAD é uma versão que traz melhorias e ajustes diversos.

Confira abaixo todos os detalhes dessa atualização.

## Novas funcionalidades

### Horário de Funcionamento

Foi implementada uma nova funcionalidade que permite configurar um horário de funcionamento por equipamento, evitando assim que usuários acessem o sistema em horários indevidos.

### SIAD Forms

Lançamento do novo módulo de formulários dinâmicos que permite a estruturação, gestão e acompanhamento de fluxos procedimentais e etapas de atendimento de forma integrada. O SIAD Forms traz flexibilidade total para a criação de campos personalizados — com suporte a condicionantes lógicas (campos dependentes pai/filho) e estruturas de dados repetidores (repeaters) —, além de um controle de acesso refinado por perfis. Entre os principais benefícios, destacam-se a otimização na coleta de respostas de protocolos, a garantia da integridade e da preservação do histórico de dados em consultas internas e externas (mesmo após a evolução de versões do formulário) e uma experiência de acompanhamento público fluida e segura, promovendo maior agilidade e transparência a todo o processo.

### Usuários - Passkeys

Foi implementada a autenticação por passkey no SIAD, permitindo um método de acesso mais seguro e sem uso de senha tradicional. Para configurar, o usuário deve acessar a tela de alteração de senha, informar um nome identificador para a chave (por exemplo, “Notebook do trabalho” ou “Celular pessoal”) e seguir o fluxo de cadastro utilizando o dispositivo compatível (biometria, PIN ou reconhecimento facial). Durante o processo, o navegador solicitará a confirmação por meio do gerenciador de credenciais do sistema operacional ou dispositivo. Após o registro, a passkey poderá ser utilizada para autenticação rápida e segura, vinculada ao dispositivo e protegida por mecanismos locais de segurança.

## Melhorias

### Cadastro de Pessoas - Nova escolaridade

Foi adicionada a escolaridade "Ensino Técnico Incompleto".

### Projetos - Melhorias em textos explicativos

Os textos explicativos do SIAD Projetos foram melhorados.

### Infraestrutura - Migração do ambiente de desenvolvimento

O ambiente de desenvolvimento foi migrado para um novo servidor dedicado.

### Usuários - Senha padrão

Ao cadastrar novos usuários, não será mais exibida a senha padrão "mudar123". Ao invés disso, o sistema permitirá gerar senhas seguras para novos usuários.

## Ajustes

### Atendimento - Correção de impresso de atendimento excluído

Foi corrigido o comportamento que permitia usuários imprimirem atendimentos excluídos.

### Atendimento - Correção do usuário padrão

Foi corrigido o bug em que o usuário padrão não estava sendo gravado nos formulários externos de atendimento.

### Auditoria - Nome completo do modelo

A trilha de auditoria foi ajustada para armazenar o nome completo do modelo (namespace) das informações armazenadas, para evitar ambiguidades.

### Transcidadania - Correção de alerta de escola

Foi corrigida a exibição do alerta de escola na tela de cadastro do Transcidadania.

### Usuário - Correção de erro ao fazer login

Foi corrigido um erro de expiração que era exibido para novos usuários.
