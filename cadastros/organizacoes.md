# Organizações

## Cadastro de Organizações

Organizações são as entidades parceiras (ONGs, associações, OSCs) que operam serviços em conjunto com a SMDHC. No SIAD, a organização é identificada pelo CNPJ e pode estar vinculada a equipamentos, benefícios e programas.

Para gerenciar as organizações, acesse **Cadastros > Organizações**.

***

### Listagem de organizações

<table><thead><tr><th width="234">Coluna</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>CNPJ</strong></td><td>CNPJ formatado. Pesquisável com ou sem pontuação.</td></tr><tr><td><strong>Razão Social</strong></td><td>Nome oficial, com o nome fantasia em descrição.</td></tr><tr><td><strong>Nome do Responsável</strong></td><td>Pessoa responsável pela organização, com e-mail em descrição.</td></tr><tr><td><strong>Contato</strong></td><td>Telefone de contato, com e-mail em descrição.</td></tr><tr><td><strong>Registrado</strong></td><td>Data de criação.</td></tr></tbody></table>

A listagem permite buscar por CNPJ, razão social, nome fantasia, contato ou e-mail. O filtro **Registro excluído** permite visualizar organizações excluídas.

***

### Criar uma organização

Clique em **"Cadastrar Organização"** no topo da listagem. O formulário está dividido em quatro seções.

#### Dados da Organização

<table><thead><tr><th width="214.333251953125">Campo</th><th width="128" align="center">Obrigatório</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>CNPJ</strong></td><td align="center">Sim</td><td>Informe o CNPJ e clique na <strong>lupa</strong> para consultar automaticamente a Receita Federal e preencher os demais campos. Deve ser único no sistema. Não pode ser alterado após criação.</td></tr><tr><td><strong>Razão Social</strong></td><td align="center">Sim</td><td>Nome oficial registrado na Receita. Preenchido automaticamente pela consulta de CNPJ, mas pode ser editado.</td></tr><tr><td><strong>Nome Fantasia</strong></td><td align="center">Não</td><td>Nome fantasia da organização.</td></tr><tr><td><strong>E-mail da organização</strong></td><td align="center">Não</td><td>Endereço de e-mail institucional.</td></tr><tr><td><strong>Contato da Organização</strong></td><td align="center">Não</td><td>Telefone de contato principal.</td></tr><tr><td><strong>Outros Contatos</strong></td><td align="center">Não</td><td>Repeater em formato de tabela para registrar múltiplos contatos adicionais (descrição, contato, observações).</td></tr></tbody></table>

#### Dados do Responsável

<table><thead><tr><th width="235.3333740234375">Campo</th><th width="132.3333740234375" align="center">Obrigatório</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Nome do(a) Responsável</strong></td><td align="center">Não</td><td>Nome da pessoa responsável legal pela organização.</td></tr><tr><td><strong>E-mail do(a) Responsável</strong></td><td align="center">Não</td><td>E-mail de contato do responsável.</td></tr></tbody></table>

#### Dados de Localização

<table><thead><tr><th width="159.6666259765625">Campo</th><th width="134.666748046875" align="center">Obrigatório</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>CEP</strong></td><td align="center">Não</td><td>CEP da sede. Possui botão de consulta que preenche endereço, bairro, distrito e município automaticamente.</td></tr><tr><td><strong>Endereço</strong></td><td align="center">Não</td><td>Logradouro.</td></tr><tr><td><strong>Número</strong></td><td align="center">Não</td><td>Número do endereço.</td></tr><tr><td><strong>Complemento</strong></td><td align="center">Não</td><td>Complemento.</td></tr><tr><td><strong>Bairro</strong></td><td align="center">Não</td><td>Bairro.</td></tr><tr><td><strong>Distrito</strong></td><td align="center">Não</td><td>Distrito administrativo. Visível apenas para organizações em São Paulo.</td></tr><tr><td><strong>Município</strong></td><td align="center">Não</td><td>Município da sede. Preenchido automaticamente pela consulta de CEP.</td></tr></tbody></table>

#### Outros

<table><thead><tr><th width="182">Campo</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Observações</strong></td><td>Campo de texto rico para registrar informações complementares sobre a organização.</td></tr></tbody></table>

***

### Consulta automática de CNPJ

Ao informar o CNPJ e clicar no botão de consulta (lupa), o sistema busca os dados na Receita Federal e preenche automaticamente:

* Razão social e nome fantasia
* Nome e e-mail do responsável
* E-mail e contato da organização
* Endereço completo (CEP, logradouro, número, complemento, bairro, município, distrito)

Caso a organização já exista no banco pelo CNPJ informado, o sistema reutiliza o cadastro existente.

***

### Sidebar da organização

Ao visualizar ou editar uma organização, a sidebar lateral oferece navegação entre as páginas:

<table><thead><tr><th width="237.3333740234375">Item</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Consultar Dados</strong></td><td>Ficha de cadastro em modo leitura.</td></tr><tr><td><strong>Atualizar Cadastro</strong></td><td>Formulário de edição.</td></tr><tr><td><strong>Equipamentos</strong></td><td>Lista de equipamentos operados pela organização (com link para cada equipamento).</td></tr><tr><td><strong>Credenciais de Acesso</strong></td><td>Gerenciamento de acessos de portal para a organização.</td></tr><tr><td><strong>Anexos</strong></td><td>Upload e gerenciamento de documentos vinculados.</td></tr><tr><td><strong>Benefícios</strong></td><td>Lista de benefícios (SIAD Benefícios) habilitados para a organização.</td></tr></tbody></table>

***

### Equipamentos vinculados

A página **Equipamentos** lista todos os equipamentos que possuem esta organização como responsável. Exibe código SIAD, nome abreviado e temática, com link direto para o cadastro do equipamento.

***

### Credenciais de acesso

A página **Credenciais de Acesso** permite criar e gerenciar acessos de portal para a organização. É utilizada quando a organização parceira precisa acessar funcionalidades específicas do SIAD (ex: Programa Cidade Solidária).

#### Criar credencial

Clique em **"Cadastrar Credencial de Acesso"**:

<table><thead><tr><th width="163">Campo</th><th width="135.3333740234375" align="center">Obrigatório</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Módulo</strong></td><td align="center">Sim</td><td>Selecione qual módulo a credencial dará acesso. Não é permitido criar duas credenciais para o mesmo módulo.</td></tr><tr><td><strong>Senha</strong></td><td align="center">—</td><td>Gerada automaticamente (12 caracteres aleatórios). Exibida uma única vez na criação — deve ser anotada imediatamente.</td></tr><tr><td><strong>Expira em</strong></td><td align="center">Não</td><td>Data/hora de expiração. Após esse momento, a credencial é bloqueada (destacada em vermelho na listagem).</td></tr><tr><td><strong>Observações</strong></td><td align="center">Não</td><td>Notas internas sobre a credencial.</td></tr></tbody></table>

#### Gerenciar credenciais

A listagem exibe módulo, expiração, datas de criação/alteração e último acesso. Ações disponíveis:

* **Visualizar**: ver detalhes da credencial
* **Editar**: alterar expiração e observações
* **Excluir**: remover a credencial
* **Reiniciar senha**: gera uma nova senha aleatória (exibida em notificação — anotar imediatamente)

Credenciais expiradas ou excluídas aparecem com fundo vermelho.

***

### Anexos

A página **Anexos** permite fazer upload de documentos relacionados à organização (contratos, portarias, atas, certidões etc.).

<table><thead><tr><th width="152.3333740234375">Campo</th><th width="131" align="center">Obrigatório</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Descrição</strong></td><td align="center">Sim</td><td>Descrição do documento.</td></tr><tr><td><strong>Anexo</strong></td><td align="center">Sim</td><td>Upload do arquivo. Aceita PDF, DOC, XLS, imagens, ZIP. Máximo 50MB.</td></tr></tbody></table>

Anexos podem ser visualizados, editados, excluídos e restaurados. Download e abertura direta estão disponíveis.

***

### Benefícios habilitados

A página **Benefícios** lista os benefícios do SIAD Benefícios que possuem esta organização vinculada. A vinculação é feita pela configuração de cada benefício (não pela organização em si). É possível remover a habilitação diretamente por esta página.

***

### Regras de exclusão

Uma organização só pode ser excluída se **não possuir** nenhum dos seguintes vínculos:

* Usuários (credenciais) vinculados (ativos ou excluídos)
* Lotes do Cidade Solidária vinculados
* Remessas do Cidade Solidária vinculadas

Caso exista algum desses vínculos, a exclusão é bloqueada.

***

### Permissões

<table><thead><tr><th width="310">Permissão</th><th>Descrição</th></tr></thead><tbody><tr><td><code>ORGANIZACAO_ACESSAR</code></td><td>Ver a listagem de organizações.</td></tr><tr><td><code>ORGANIZACAO_CONSULTAR</code></td><td>Visualizar detalhes de uma organização.</td></tr><tr><td><code>ORGANIZACAO_CADASTRAR</code></td><td>Criar novas organizações.</td></tr><tr><td><code>ORGANIZACAO_ALTERAR</code></td><td>Editar organizações existentes.</td></tr><tr><td><code>ORGANIZACAO_EXCLUIR</code></td><td>Excluir organizações (com validação de vínculos).</td></tr><tr><td><code>ORGANIZACAO_REATIVAR</code></td><td>Restaurar organizações excluídas.</td></tr><tr><td><code>ORGANIZACAO_MANTER_CREDENCIAIS</code></td><td>Criar, editar, excluir e reiniciar senhas de credenciais de acesso.</td></tr></tbody></table>
