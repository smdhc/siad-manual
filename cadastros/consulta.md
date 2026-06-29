# Equipamentos

## Cadastro de Equipamentos

Equipamentos são as unidades de atendimento e serviço da SMDHC — CRCM, CRPIR, Núcleos de Ouvidoria, Coordenações, RCEs e demais pontos da rede. No SIAD, o equipamento é a entidade central que vincula profissionais, atendimentos, benefícios e programas. Todo usuário do sistema deve estar vinculado a um equipamento.

Para gerenciar os equipamentos, acesse **Cadastros > Equipamentos**.

***

### Listagem de equipamentos

A listagem exibe todos os equipamentos da rede com as seguintes colunas:

<table><thead><tr><th width="244.6666259765625">Coluna</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Código</strong></td><td>Código SIAD gerado automaticamente (formato: SIAD + 5 dígitos + verificador).</td></tr><tr><td><strong>Nome do Equipamento</strong></td><td>Nome abreviado. Exibe a organização responsável como descrição (ou "Administração Direta").</td></tr><tr><td><strong>Tipo</strong></td><td>Tipo do equipamento com a temática em descrição.</td></tr><tr><td><strong>Subprefeitura</strong></td><td>Subprefeitura com o distrito em descrição.</td></tr><tr><td><strong>Contato</strong></td><td>Dados de contato.</td></tr><tr><td><strong>Marcadores</strong></td><td>Tags/marcadores vinculados (oculto por padrão).</td></tr></tbody></table>

### Filtros disponíveis

<table><thead><tr><th width="288.666748046875">Filtro</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Tipo de Equipamento</strong></td><td>Filtra por tipo (CCM, CRAS, Coordenadoria etc.).</td></tr><tr><td><strong>Temática</strong></td><td>Filtra por temática (Mulheres, Igualdade Racial, LGBTQIA+ etc.).</td></tr><tr><td><strong>Organização Responsável</strong></td><td>Filtra por organização.</td></tr><tr><td><strong>Distrito</strong></td><td>Filtra por distrito.</td></tr><tr><td><strong>Subprefeitura</strong></td><td>Filtra por subprefeitura.</td></tr><tr><td><strong>Módulos Habilitados</strong></td><td>Filtra por módulos ativos. Visível apenas para administradores.</td></tr><tr><td><strong>Situação</strong></td><td>Ativos, Inativos ou ambos. Padrão: somente ativos.</td></tr><tr><td><strong>Realiza atendimentos?</strong></td><td>Sim / Não.</td></tr><tr><td><strong>Rede de atendimento SMDHC?</strong></td><td>Sim / Não.</td></tr><tr><td><strong>Sigiloso</strong></td><td>Sim / Não.</td></tr><tr><td><strong>Marcadores</strong></td><td>Filtra por marcadores vinculados.</td></tr></tbody></table>

***

### Criar um equipamento

Clique em **Criar** no topo da listagem. O formulário está dividido em duas seções: Dados Cadastrais e Localização.

#### Dados Cadastrais

<table><thead><tr><th width="247.3333740234375">Campo</th><th width="112.3333740234375" align="center">Obrigatório</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Nome completo</strong></td><td align="center">Sim</td><td>Nome oficial do equipamento. Único no sistema. Ex: "CENTRO DE CIDADANIA DA MULHER ITAQUERA".</td></tr><tr><td><strong>Nome curto/abreviado</strong></td><td align="center">Sim</td><td>Nome abreviado utilizado em listagens e seleções. Único. Ex: "CCM ITAQUERA".</td></tr><tr><td><strong>Tipo de Equipamento</strong></td><td align="center">Sim</td><td>Classificação do equipamento (ex: CCM, CRAS, CREAS, Centro de Acolhida, Coordenadoria).</td></tr><tr><td><strong>Temática</strong></td><td align="center">Não</td><td>Temática à qual o equipamento pertence (Mulheres, Igualdade Racial, LGBTQIA+, Pop Rua, Imigrantes etc.).</td></tr><tr><td><strong>Organização Responsável</strong></td><td align="center">Não</td><td>Organização parceira que opera o equipamento. Desabilitado quando "Administração Direta" está ativo.</td></tr><tr><td><strong>Horário de Funcionamento</strong></td><td align="center">Não</td><td>Texto descritivo do horário de atendimento ao público (ex: "Segunda a sexta, 8h às 17h").</td></tr><tr><td><strong>Módulos habilitados</strong></td><td align="center">Não</td><td>Define quais módulos do SIAD estarão disponíveis para os profissionais deste equipamento. Editável apenas por administradores. Opções: Atendimento, Transcidadania, Planejamento, Programa de Geração de Renda, Programa Cidade Solidária.</td></tr><tr><td><strong>Realiza atendimentos?</strong></td><td align="center">Não</td><td>Indica se o equipamento registra atendimentos no módulo de Atendimento.</td></tr><tr><td><strong>Rede de Atendimento SMDHC?</strong></td><td align="center">Não</td><td>Indica se o equipamento compõe a rede oficial de atendimento. Se habilitado, será exibido no site da <a href="https://rededireitoshumanos.prefeitura.sp.gov.br/">Rede de Atendimento SMDHC</a>.</td></tr><tr><td><strong>Administração Direta?</strong></td><td align="center">Não</td><td>Quando ativo, indica que o equipamento é operado diretamente pela prefeitura (sem organização parceira). Desabilita o campo Organização.</td></tr><tr><td><strong>Sigiloso?</strong></td><td align="center">Não</td><td>Quando ativo, oculta todos os dados de contato e localização do equipamento. Usado para equipamentos de proteção (ex: casas-abrigo).</td></tr><tr><td><strong>Dados para contato</strong></td><td align="center">Não</td><td>Telefone(s) de contato. Oculto quando sigiloso.</td></tr><tr><td><strong>E-mail</strong></td><td align="center">Não</td><td>Endereço de e-mail institucional do equipamento.</td></tr><tr><td><strong>Data Início de Vigência</strong></td><td align="center">Não</td><td>Data a partir da qual o equipamento está ativo.</td></tr><tr><td><strong>Data Fim de Vigência</strong></td><td align="center">Não</td><td>Data de encerramento. Quando preenchida com data passada, o equipamento é considerado inativo.</td></tr><tr><td><strong>Categoria (slug)</strong></td><td align="center">Não</td><td>Identificador para integração com o site da Rede de Atendimento SMDHC.</td></tr><tr><td><strong>Marcadores</strong></td><td align="center">Não</td><td>Tags para classificação adicional. É possível criar novos marcadores diretamente pelo botão "Novo Marcador".</td></tr><tr><td><strong>Observações</strong></td><td align="center">Não</td><td>Campo de texto livre.</td></tr></tbody></table>

#### Localização

Seção oculta quando o equipamento é **sigiloso**.

<table><thead><tr><th width="191.6666259765625">Campo</th><th width="137.3333740234375" align="center">Obrigatório</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>CEP</strong></td><td align="center">Não</td><td>CEP do equipamento. Possui botão de consulta automática que preenche endereço, bairro e distrito.</td></tr><tr><td><strong>Endereço</strong></td><td align="center">Não</td><td>Logradouro completo.</td></tr><tr><td><strong>Número</strong></td><td align="center">Não</td><td>Número do endereço.</td></tr><tr><td><strong>Complemento</strong></td><td align="center">Não</td><td>Complemento (sala, andar etc.).</td></tr><tr><td><strong>Bairro</strong></td><td align="center">Não</td><td>Bairro do equipamento.</td></tr><tr><td><strong>Distrito</strong></td><td align="center">Sim</td><td>Distrito administrativo. Exibe a subprefeitura correspondente automaticamente.</td></tr><tr><td><strong>Latitude</strong></td><td align="center">Não</td><td>Coordenada geográfica (formato: -23.XXXXX).</td></tr><tr><td><strong>Longitude</strong></td><td align="center">Não</td><td>Coordenada geográfica (formato: -46.XXXXX).</td></tr></tbody></table>

***

### Código SIAD

Ao criar um equipamento, o sistema gera automaticamente um **código SIAD** único seguindo a fórmula:

* Prefixo: `SIAD`
* Raiz: ID × 7, formatado com 5 dígitos
* Verificador: resto da divisão da raiz por 9

Exemplo: ID 2 → `SIAD000145`

O código é exibido na tela de edição e na visualização, e pode ser copiado com um clique.

***

### Equipamentos sigilosos

Quando a flag **"Sigiloso"** está ativa:

* Toda a seção de Localização fica oculta no formulário
* O campo de contato é automaticamente apagado ao salvar
* Na visualização, exibe um alerta: "Atenção: Equipamento sigiloso!"
* Endereço, CEP, bairro, distrito, latitude e longitude são removidos do banco

Essa funcionalidade é utilizada para equipamentos de proteção cuja localização não deve ser divulgada.

***

### Módulos habilitados

O campo **"Módulos habilitados"** define quais funcionalidades do SIAD estarão acessíveis para os profissionais vinculados ao equipamento:

<table><thead><tr><th width="260">Módulo</th><th>Efeito quando habilitado</th></tr></thead><tbody><tr><td><strong>Atendimento</strong></td><td>Habilita o módulo de Atendimento (registrar atendimentos, tipos de atendimento).</td></tr><tr><td><strong>Transcidadania</strong></td><td>Habilita o módulo Transcidadania (cadastro, frequências, PIA).</td></tr><tr><td><strong>Programa de Geração de Renda</strong></td><td>Habilita o módulo Geração de Renda (cadastro, PIA).</td></tr><tr><td><strong>Planejamento</strong></td><td>Habilita o módulo de Planejamento.</td></tr><tr><td><strong>Programa Cidade Solidária</strong></td><td>Habilita funcionalidades do Cidade Solidária.</td></tr></tbody></table>

Se nenhum módulo estiver habilitado, os profissionais do equipamento terão acesso apenas às funcionalidades básicas (cadastro de pessoas, consultas).

> **Atenção**: este campo só pode ser editado por administradores do sistema.

***

### Configurações do equipamento

Além dos dados cadastrais, cada equipamento possui uma página de **Configurações** (acessível pela sidebar > "Configurações") que controla parâmetros operacionais.

#### Horário de funcionamento no SIAD

Define os dias e horários em que os profissionais do equipamento podem acessar o sistema:

<table><thead><tr><th width="210.6666259765625">Campo</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Horário Início</strong></td><td>Hora a partir da qual o acesso é permitido. Se vazio, assume 00:00.</td></tr><tr><td><strong>Horário Fim</strong></td><td>Hora até a qual o acesso é permitido. Se vazio, assume 23:59.</td></tr><tr><td><strong>Dias da Semana</strong></td><td>Checkboxes para cada dia. Todos marcados por padrão.</td></tr></tbody></table>

Quando configurado:

* O login é bloqueado fora do horário (com mensagem explicativa)
* Usuários logados são deslogados automaticamente ao fim do expediente
* Um banner de aviso aparece minutos antes do encerramento (tempo configurável globalmente)
* Usuários com permissão `ADMIN` ou `EQUIPAMENTO_ACESSAR_FORA_HORARIO` não são afetados

#### Prazo para edição de atendimentos

<table><thead><tr><th width="188">Campo</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Prazo em dias</strong></td><td>Limita o período para inserção, edição ou exclusão de atendimentos, considerando a diferença entre a data atual e a data do atendimento. Se configurado, atendimentos fora do prazo ficam bloqueados. Pode ser sobrescrito por configuração do tipo de atendimento ou grupo de atendimento.</td></tr></tbody></table>

***

### Benefícios habilitados

A página **"Benefícios"** na sidebar lista os benefícios do SIAD Benefícios vinculados ao equipamento. Essa vinculação é gerenciada pelo módulo de Benefícios (na configuração de cada benefício) e determina quais benefícios os técnicos do equipamento podem operar.

***

### Permissões

<table><thead><tr><th width="300">Permissão</th><th>Descrição</th></tr></thead><tbody><tr><td><code>EQUIPAMENTO_ACESSAR</code></td><td>Ver a listagem de equipamentos.</td></tr><tr><td><code>EQUIPAMENTO_CONSULTAR</code></td><td>Visualizar os detalhes de um equipamento.</td></tr><tr><td><code>EQUIPAMENTO_CADASTRAR</code></td><td>Criar novos equipamentos.</td></tr><tr><td><code>EQUIPAMENTO_ALTERAR</code></td><td>Editar equipamentos existentes.</td></tr><tr><td><code>EQUIPAMENTO_CONFIGURAR</code></td><td>Acessar a página de Configurações (horário, prazo de atendimento).</td></tr><tr><td><code>EQUIPAMENTO_ACESSAR_FORA_HORARIO</code></td><td>Permite login fora do horário configurado no equipamento.</td></tr></tbody></table>

> **Nota**: equipamentos não podem ser excluídos pelo sistema (delete sempre retorna falso). Para inativar, preencha a "Data Fim de Vigência" com uma data passada.

***

### Situação ativa/inativa

Um equipamento é considerado **inativo** quando sua "Data Fim de Vigência" é anterior à data atual. Equipamentos inativos:

* Aparecem com alerta na visualização: "Atenção: Equipamento inativo!"
* Podem ser filtrados na listagem pelo filtro "Situação"
* Continuam existindo no sistema (os usuários vinculados permanecem, mas podem ter restrições operacionais)
