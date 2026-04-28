---
description: 'Data de lançamento: a definir'
---

# Versão 7.2.0

A **versão 7.2.0** do SIAD é uma versão que traz melhorias e ajustes diversos.

Confira abaixo todos os detalhes dessa atualização.

## Novas funcionalidades

### Usuários - Passkeys

Foi implementada a autenticação por passkey no SIAD, permitindo um método de acesso mais seguro e sem uso de senha tradicional. Para configurar, o usuário deve acessar a tela de alteração de senha, informar um nome identificador para a chave (por exemplo, “Notebook do trabalho” ou “Celular pessoal”) e seguir o fluxo de cadastro utilizando o dispositivo compatível (biometria, PIN ou reconhecimento facial). Durante o processo, o navegador solicitará a confirmação por meio do gerenciador de credenciais do sistema operacional ou dispositivo. Após o registro, a passkey poderá ser utilizada para autenticação rápida e segura, vinculada ao dispositivo e protegida por mecanismos locais de segurança.

## Ajustes

### Auditoria - Nome completo do modelo

A trilha de auditoria foi ajustada para armazenar o nome completo do modelo (namespace) das informações armazenadas, para evitar ambiguidades.
