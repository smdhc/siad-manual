# Usuários

## Cadastro de Usuários

Usuários são os profissionais que acessam o SIAD para registrar atendimentos, cadastrar pessoas, gerenciar benefícios e operar os demais módulos. Cada usuário é vinculado a um equipamento e possui um ou mais perfis que determinam suas permissões no sistema.

Para gerenciar os usuários, acesse **Controle de Acesso > Usuários** (no painel Admin) ou **Cadastros > Profissionais** (no painel Atendimento).

> **Nota**: no painel de Atendimento, a listagem exibe apenas os profissionais do equipamento do usuário logado. O gerenciamento completo (todos os equipamentos) é feito pelo painel Admin.

***

### Listagem de usuários

<table><thead><tr><th width="254">Coluna</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Nome do Usuário</strong></td><td>Nome completo do profissional.</td></tr><tr><td><strong>CPF</strong></td><td>CPF formatado.</td></tr><tr><td><strong>E-mail</strong></td><td>E-mail de acesso.</td></tr><tr><td><strong>Equipamento</strong></td><td>Equipamento de vínculo (visível no painel Admin).</td></tr><tr><td><strong>Data de Criação</strong></td><td>Quando o cadastro foi criado (painel Admin).</td></tr><tr><td><strong>Criado por</strong></td><td>Quem cadastrou o usuário (painel Admin).</td></tr><tr><td><strong>Ocupação</strong></td><td>Ocupação profissional (ex: Assistente Social, Psicólogo).</td></tr><tr><td><strong>Conselho de Classe</strong></td><td>Sigla e número do conselho (ex: CRP 12345).</td></tr><tr><td><strong>Último Acesso</strong></td><td>Data/hora do último login.</td></tr><tr><td><strong>É do Equipamento?</strong></td><td>Se é profissional do equipamento (oculto por padrão).</td></tr><tr><td><strong>Perfis</strong></td><td>Perfis atribuídos em formato de badge (visível para admins).</td></tr></tbody></table>

Usuários excluídos (inativos) aparecem com fundo vermelho.

### Filtros disponíveis (painel Admin)

<table><thead><tr><th width="321.3333740234375">Filtro</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Equipamento</strong></td><td>Filtra por equipamento de vínculo.</td></tr><tr><td><strong>Temática do Equipamento</strong></td><td>Filtra por temática.</td></tr><tr><td><strong>Tipo de Equipamento</strong></td><td>Filtra por tipo de equipamento.</td></tr><tr><td><strong>Perfil</strong></td><td>Filtra por perfil atribuído.</td></tr><tr><td><strong>Profissional do Equipamento?</strong></td><td>Filtra quem está marcado como profissional (aparece nos atendimentos).</td></tr><tr><td><strong>Período de cadastro</strong></td><td>Filtra por intervalo de datas de criação.</td></tr><tr><td><strong>CPF</strong></td><td>Busca direta por CPF.</td></tr><tr><td><strong>Exibir Organizações</strong></td><td>Permite alternar entre usuários normais e credenciais de organizações.</td></tr><tr><td><strong>Registro excluído</strong></td><td>Permite incluir ou exibir apenas usuários excluídos.</td></tr></tbody></table>

***

### Criar um usuário

Clique em **"Cadastrar Usuário"** no topo da listagem. O formulário é inteligente e se adapta conforme a verificação do CPF.

#### Passo 1 — Informar o CPF

Ao digitar o CPF e sair do campo, o sistema verifica automaticamente:

* **"Usuário não cadastrado"**: o CPF não existe na base. O formulário exibe todos os campos para preenchimento completo.
* **"Usuário já cadastrado"**: o CPF já existe vinculado a outro equipamento. O formulário preenche nome e e-mail automaticamente e permite criar um **novo vínculo** com outro equipamento.

#### Campos do formulário

**Dados do Profissional**

<table><thead><tr><th width="212.3333740234375">Campo</th><th width="162.333251953125" align="center">Obrigatório</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>CPF</strong></td><td align="center">Sim</td><td>CPF do profissional. Validação automática. Não pode ser alterado após criação.</td></tr><tr><td><strong>Senha inicial</strong></td><td align="center">Condicional</td><td>Obrigatória para novos usuários (quando não for enviar por e-mail). Possui botão para gerar senha segura automaticamente. Mínimo 8 caracteres.</td></tr><tr><td><strong>Nome completo</strong></td><td align="center">Sim</td><td>Nome do profissional. Mínimo 3 caracteres.</td></tr><tr><td><strong>E-mail</strong></td><td align="center">Sim</td><td>Endereço de e-mail. Deve ser único entre os usuários ativos.</td></tr><tr><td><strong>Ocupação</strong></td><td align="center">Sim</td><td>Ocupação profissional (ex: Assistente Social, Psicólogo/a, Advogado/a, Técnico Administrativo).</td></tr><tr><td><strong>Tipo de conselho</strong></td><td align="center">Não</td><td>Conselho de classe (ex: CRP, CRESS, OAB).</td></tr><tr><td><strong>Número do conselho</strong></td><td align="center">Condicional</td><td>Obrigatório quando tipo de conselho é preenchido.</td></tr></tbody></table>

**Permissões (visível apenas para administradores)**

<table><thead><tr><th width="223">Campo</th><th width="121.3333740234375" align="center">Obrigatório</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Equipamento</strong></td><td align="center">Sim</td><td>Equipamento ao qual o usuário será vinculado. Na criação, lista apenas equipamentos onde o CPF ainda não tem vínculo. Não pode ser alterado após criação.</td></tr><tr><td><strong>Perfis</strong></td><td align="center">Não</td><td>Perfis de permissão atribuídos ao usuário. Permite múltipla seleção. O perfil "Administrador" só é listado para quem já é admin.</td></tr><tr><td><strong>É profissional do equipamento?</strong></td><td align="center">Sim</td><td>Quando "Sim", o usuário aparece como opção no campo "Profissional" ao registrar atendimentos.</td></tr><tr><td><strong>Enviar notificação por e-mail?</strong></td><td align="center">Não</td><td>Quando "Sim", envia e-mail com link de definição de senha ao criar. Visível apenas quando o usuário é novo e possui perfis selecionados.</td></tr></tbody></table>

***

### Múltiplos vínculos (mesmo CPF em vários equipamentos)

Uma característica do SIAD é que um mesmo profissional pode ter **vínculos com múltiplos equipamentos**. Cada vínculo é um registro separado com seu próprio equipamento e perfis.

Ao criar um segundo vínculo para um CPF existente:

* O sistema exibe um aviso explicando que será criado um novo vínculo
* O campo equipamento lista apenas equipamentos onde o CPF ainda não está vinculado
* A senha permanece a mesma de qualquer outro vínculo do CPF
* Alterações em nome, e-mail e ocupação são sincronizadas entre todos os vínculos do CPF

***

### Editar usuário

Ao editar, os seguintes campos podem ser alterados:

* Nome, e-mail, ocupação, conselho de classe, número do conselho
* Perfis atribuídos
* É profissional do equipamento?

Os campos **CPF** e **Equipamento** não podem ser alterados.

> **Nota sobre sincronização**: ao salvar, as alterações de nome, e-mail, senha e ocupação são propagadas automaticamente para todos os vínculos do mesmo CPF em outros equipamentos.

***

### Ações sobre usuários

#### Excluir (desativar)

A exclusão é um soft delete — o usuário perde acesso ao sistema mas permanece no banco. Registros excluídos ficam com fundo vermelho na listagem.

#### Restaurar

Restaura um usuário excluído. A restauração só é permitida se **não existir outro usuário ativo com o mesmo CPF no mesmo equipamento**.

#### Reiniciar senha

Duas modalidades:

<table><thead><tr><th width="248">Modalidade</th><th>Comportamento</th></tr></thead><tbody><tr><td><strong>Com envio por e-mail</strong></td><td>Envia um link de redefinição de senha para o e-mail do usuário. O usuário mantém a senha atual até usar o link.</td></tr><tr><td><strong>Sem envio por e-mail</strong></td><td>Gera uma senha temporária segura (formato: <code>xxxxxx-xxxxxx-xxxxxx</code>) e exibe na tela em notificação persistente. O administrador deve anotar e repassar ao usuário.</td></tr></tbody></table>

#### Gerar link de redefinição

Gera uma URL de redefinição de senha que pode ser copiada e enviada manualmente ao usuário (via WhatsApp, outro e-mail etc.). Útil quando o e-mail cadastrado não está acessível.

***

### Geração de senha segura

O sistema gera senhas no formato `xxxxxx-xxxxxx-xxxxxx` (3 blocos de 6 caracteres separados por hífen) contendo:

* 16 letras minúsculas
* 1 letra maiúscula
* 1 dígito numérico

Caracteres ambíguos (0, O, l, 1, I) são evitados para facilitar a leitura.

***

### Notificação por e-mail na criação

Quando o toggle "Enviar notificação por e-mail" está ativo e o usuário é novo (CPF não existia):

* O sistema gera um link de definição de senha
* Envia um e-mail ao usuário com o link
* O usuário não recebe senha em texto — define sua própria senha pelo link

Quando o toggle está desativado ou o CPF já existia:

* O administrador deve informar a senha manualmente ou gerar uma automática
* A senha é exibida apenas uma vez na tela

***

### Permissões

<table><thead><tr><th width="254.6666259765625">Permissão</th><th>Descrição</th></tr></thead><tbody><tr><td><code>USUARIO_ACESSAR</code></td><td>Ver a listagem de usuários.</td></tr><tr><td><code>USUARIO_CONSULTAR</code></td><td>Visualizar detalhes de um usuário.</td></tr><tr><td><code>USUARIO_CADASTRAR</code></td><td>Criar novos usuários.</td></tr><tr><td><code>USUARIO_ALTERAR</code></td><td>Editar usuários existentes.</td></tr><tr><td><code>USUARIO_EXCLUIR</code></td><td>Desativar (soft delete) usuários.</td></tr><tr><td><code>USUARIO_REATIVAR</code></td><td>Restaurar usuários desativados.</td></tr><tr><td><code>USUARIO_REINICIAR_SENHA</code></td><td>Reiniciar senha e gerar links de redefinição.</td></tr></tbody></table>

***

### Visibilidade por painel

<table><thead><tr><th width="174.6666259765625">Painel</th><th>Comportamento</th></tr></thead><tbody><tr><td><strong>Admin</strong></td><td>Listagem completa de todos os usuários do sistema, com todos os filtros e ações.</td></tr><tr><td><strong>Atendimento</strong></td><td>Lista apenas profissionais (<code>is_profissional_equipamento = Sim</code>) do equipamento do usuário logado. Label: "Profissionais". Sem filtros avançados. Exibe aviso de que o cadastro é feito via e-mail de suporte.</td></tr></tbody></table>
