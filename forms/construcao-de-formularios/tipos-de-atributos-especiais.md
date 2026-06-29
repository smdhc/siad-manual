# Tipos de Atributos Especiais

## Introdução

Alguns tipos de atributo possuem comportamentos avançados que vão além de simplesmente coletar um dado. Esta página detalha como configurar e utilizar os tipos CEP, CNPJ, Pontuação/Resultado e Repeater.

***

### CEP — Preenchimento automático de endereço

O tipo **CEP** permite que, ao informar um CEP válido, outros campos do formulário sejam preenchidos automaticamente com os dados do endereço (logradouro, bairro, município, distrito e UF).

#### Como funciona

Quando o respondente digita um CEP e sai do campo (ou pressiona Enter), o sistema consulta a base de endereços e preenche automaticamente os campos mapeados. Se o CEP não for encontrado, os campos permanecem vazios para preenchimento manual.

#### Pré-requisitos

Para que o preenchimento automático funcione, é necessário que os campos de destino (logradouro, bairro etc.) já existam no mesmo formulário como atributos independentes. Eles devem ser criados antes de configurar o mapeamento no CEP.

Os tipos aceitos para os campos de destino são:

<table><thead><tr><th width="184.6666259765625">Campo de destino</th><th>Tipos aceitos</th></tr></thead><tbody><tr><td>Logradouro</td><td>Texto Curto, Texto Longo</td></tr><tr><td>Bairro</td><td>Texto Curto, Texto Longo</td></tr><tr><td>Município</td><td>Texto Curto, Texto Longo ou Município</td></tr><tr><td>Distrito</td><td>Texto Curto, Texto Longo ou Distrito</td></tr><tr><td>UF</td><td>Texto Curto, Texto Longo ou UF</td></tr></tbody></table>

#### Passo a passo

1. Crie os atributos de destino no formulário (ex: "Logradouro" tipo Texto Curto, "Bairro" tipo Texto Curto, "Município" tipo Município etc.)
2. Crie o atributo do tipo **CEP**
3. Adicione todos os atributos à seção desejada
4. Ao adicionar o atributo CEP à seção, na tela **"Adicionar Atributo à Seção"**, uma área extra de configuração aparecerá com os seguintes campos de mapeamento:

<table><thead><tr><th width="222">Campo</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Campo Logradouro</strong></td><td>Selecione o atributo que receberá o logradouro retornado pela consulta.</td></tr><tr><td><strong>Campo Bairro</strong></td><td>Selecione o atributo que receberá o bairro.</td></tr><tr><td><strong>Campo Município</strong></td><td>Selecione o atributo que receberá o município (nome textual ou FK, dependendo do tipo).</td></tr><tr><td><strong>Campo Distrito</strong></td><td>Selecione o atributo que receberá o distrito.</td></tr><tr><td><strong>Campo UF</strong></td><td>Selecione o atributo que receberá a unidade federativa.</td></tr></tbody></table>

Todos os campos de mapeamento são opcionais — configure apenas os que fazem sentido para o seu formulário.

#### Observações

* Os campos de destino podem estar na mesma seção ou em seções diferentes do mesmo formulário.
* Se o campo de destino for do tipo **Município** (FK), o sistema vinculará automaticamente o ID do município correspondente. Se for do tipo Texto, preencherá com o nome.
* O mesmo vale para **Distrito** e **UF**.

***

### CNPJ — Preenchimento automático de dados empresariais

O tipo **CNPJ** funciona de forma semelhante ao CEP: ao informar um CNPJ válido, o sistema consulta a base de dados e preenche automaticamente outros campos com informações da empresa.

#### Campos disponíveis para mapeamento

Ao adicionar o atributo CNPJ à seção, a configuração exibe os seguintes campos de destino:

<table><thead><tr><th width="302">Campo</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Campo Razão Social</strong></td><td>Receberá a razão social da empresa.</td></tr><tr><td><strong>Campo Nome Fantasia</strong></td><td>Receberá o nome fantasia.</td></tr><tr><td><strong>Campo E-mail</strong></td><td>Receberá o e-mail de contato.</td></tr><tr><td><strong>Campo Telefone/Contato</strong></td><td>Receberá o telefone.</td></tr><tr><td><strong>Campo CEP</strong></td><td>Receberá o CEP do endereço da empresa.</td></tr><tr><td><strong>Campo Logradouro</strong></td><td>Receberá o logradouro.</td></tr><tr><td><strong>Campo Número</strong></td><td>Receberá o número do endereço.</td></tr><tr><td><strong>Campo Complemento</strong></td><td>Receberá o complemento.</td></tr><tr><td><strong>Campo Bairro</strong></td><td>Receberá o bairro.</td></tr><tr><td><strong>Campo Nome do Responsável</strong></td><td>Receberá o nome do responsável legal.</td></tr><tr><td><strong>Campo E-mail do Responsável</strong></td><td>Receberá o e-mail do responsável.</td></tr></tbody></table>

#### Passo a passo

1. Crie os atributos de destino desejados (todos do tipo Texto Curto ou Texto Longo, exceto E-mail que aceita o tipo E-mail, e CEP que aceita o tipo CEP)
2. Crie o atributo do tipo **CNPJ**
3. Adicione todos os atributos à seção
4. Ao configurar o CNPJ na seção, mapeie os campos de destino desejados

#### Observações

* Assim como o CEP, todos os campos de mapeamento são opcionais.
* O campo CEP de destino, se mapeado, pode acionar em cascata o preenchimento automático do endereço (se o CEP também estiver configurado com mapeamento próprio).

***

### Pontuação e Resultado — Sistema de scoring

O SIAD Forms permite criar formulários com sistema de pontuação, onde cada opção selecionada pelo respondente possui um valor numérico associado. A pontuação é calculada automaticamente e pode gerar um resultado classificatório baseado em faixas.

#### Conceitos

<table><thead><tr><th width="241.333251953125">Conceito</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Atributo com pontuação</strong></td><td>Um campo do tipo Lista ou Radio que possui valores numéricos associados a cada opção.</td></tr><tr><td><strong>Atributo Pontuação</strong></td><td>Um campo especial (tipo "Pontuação") que exibe o total calculado. Funciona como um consolidador.</td></tr><tr><td><strong>Atributo Resultado</strong></td><td>Um campo especial (tipo "Resultado") que exibe uma faixa textual baseada na pontuação alcançada.</td></tr></tbody></table>

#### Fluxo de configuração

**1. Criar os atributos com opções pontuáveis**

Crie atributos do tipo **Lista**, **Lista Dinâmica**, **Radio** ou **Radio Dinâmico** que possuam opções fixas. Esses serão os campos cujas respostas terão pontuação.

Exemplo: atributo "Frequência de atividade física" com opções "Nunca", "1-2x por semana", "3-4x por semana", "Diariamente".

**2. Criar o atributo consolidador de Pontuação**

Crie um atributo do tipo **Pontuação**. Na criação, defina o **Tipo de Agregação**:

<table><thead><tr><th width="196">Tipo</th><th>Comportamento</th></tr></thead><tbody><tr><td><strong>Soma</strong></td><td>Soma simples de todas as pontuações dos campos vinculados.</td></tr><tr><td><strong>Média Ponderada</strong></td><td>Calcula a média ponderada considerando o peso de cada campo.</td></tr></tbody></table>

**3. Criar o atributo de Resultado (opcional)**

Crie um atributo do tipo **Resultado**. Ele exibirá um texto classificatório baseado na pontuação final.

**4. Adicionar tudo à seção e configurar pontuações**

Ao adicionar os atributos do tipo Lista/Radio à seção, na tela de configuração aparecerá a seção **Pontuação** com os seguintes campos:

<table><thead><tr><th width="266">Campo</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Habilitar Pontuação</strong></td><td>Toggle que ativa o sistema de pontuação para este atributo.</td></tr><tr><td><strong>Exibir pontuação abaixo do campo</strong></td><td>Quando ativo, mostra o valor da pontuação selecionada abaixo do campo em tempo real.</td></tr><tr><td><strong>Peso</strong></td><td>Multiplicador do valor. Padrão: 1. Usado na média ponderada.</td></tr><tr><td><strong>Mapa de Valores</strong></td><td>Associação entre cada opção e seu valor numérico. Ex: "Nunca" = 0, "Diariamente" = 3.</td></tr></tbody></table>

**5. Configurar o atributo Resultado na seção**

Ao adicionar o atributo do tipo **Resultado** à seção, configure:

| Campo                     | Descrição                                                                                       |
| ------------------------- | ----------------------------------------------------------------------------------------------- |
| **Atributo de Pontuação** | Selecione qual atributo de Pontuação será utilizado como base para determinar o resultado.      |
| **Faixas de Resultado**   | Lista de faixas com mínimo, máximo e label. Ex: 0-3 = "Baixo", 4-7 = "Moderado", 8-10 = "Alto". |

**6. Footer de pontuação por seção**

Além dos campos individuais, cada seção que contenha atributos com pontuação habilitada exibe automaticamente um **footer** na seção mostrando a pontuação parcial daquela seção.

#### Comportamento em tempo real

* Ao selecionar uma opção em um campo com pontuação habilitada, o campo **Pontuação** é atualizado automaticamente (sem necessidade de salvar).
* O campo **Resultado** também é recalculado em tempo real, exibindo a faixa correspondente.
* A pontuação é recalculada considerando todos os campos com pontuação habilitada em todas as seções do formulário (cross-section).

#### Exemplo prático

Um formulário de avaliação de vulnerabilidade com 3 perguntas:

<table><thead><tr><th width="156.3333740234375">Pergunta</th><th width="389">Opções</th><th>Pontos</th></tr></thead><tbody><tr><td>Renda familiar</td><td>Até 1 SM / 1-3 SM / Acima de 3 SM</td><td>3 / 2 / 0</td></tr><tr><td>Moradia</td><td>Situação de rua / Alugado / Próprio</td><td>3 / 1 / 0</td></tr><tr><td>Escolaridade</td><td>Sem instrução / Fundamental / Médio+</td><td>2 / 1 / 0</td></tr></tbody></table>

Configuração do Resultado:

* 0 a 3: "Vulnerabilidade Baixa"
* 4 a 6: "Vulnerabilidade Moderada"
* 7 a 8: "Vulnerabilidade Alta"

***

### Repeater — Campos repetíveis

O tipo **Repeater** permite criar blocos de campos que o respondente pode repetir múltiplas vezes dentro do formulário. É a solução ideal quando o formulário precisa coletar uma lista variável de itens com a mesma estrutura.

#### Quando usar

* Cadastro de múltiplos participantes de um evento
* Listagem de documentos apresentados
* Registro de múltiplas atividades realizadas
* Qualquer cenário onde a quantidade de itens varia de uma resposta para outra

#### Como funciona

O Repeater não define seus campos internamente — ele utiliza um **formulário pré-existente** como template. Cada item adicionado pelo respondente é uma "cópia" da estrutura desse formulário vinculado.

#### Pré-requisitos

1. **Criar o formulário-template**: antes de criar o atributo Repeater, é necessário que exista um formulário separado contendo os campos que comporão cada item do repeater. Esse formulário deve ter uma versão com status **Publicada**.
2. O formulário-template funciona normalmente como qualquer outro formulário — pode ter múltiplas seções, atributos condicionais etc.

#### Passo a passo

**1. Criar o formulário-template**

Crie um formulário com os campos que cada item do repeater terá. Por exemplo, para um repeater de "Participantes", crie um formulário com campos "Nome", "CPF", "E-mail".

Publique a versão desse formulário.

**2. Criar o atributo do tipo Repeater**

No cadastro de atributos, selecione o tipo **Repeater**. Os seguintes campos adicionais aparecerão:

<table><thead><tr><th width="231.3333740234375">Campo</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Formulário</strong></td><td>Selecione o formulário-template. Somente formulários com versão publicada são listados.</td></tr><tr><td><strong>Versão do Formulário</strong></td><td>Selecione a versão publicada que será utilizada como template.</td></tr></tbody></table>

**3. Adicionar à seção e configurar**

Ao adicionar o atributo Repeater à seção, campos extras de configuração ficam disponíveis:

<table><thead><tr><th width="276">Campo</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Quantidade padrão de itens</strong></td><td>Quantos itens já aparecem preenchidos ao abrir o formulário. Padrão: 0.</td></tr><tr><td><strong>Mínimo de itens</strong></td><td>Quantidade mínima obrigatória de itens que o respondente deve preencher.</td></tr><tr><td><strong>Máximo de itens</strong></td><td>Limite máximo de itens permitidos.</td></tr><tr><td><strong>Label do botão adicionar</strong></td><td>Texto personalizado para o botão de adicionar item. Ex: "Adicionar participante".</td></tr><tr><td><strong>Bloquear reordenamento</strong></td><td>Quando ativo, impede que o respondente reordene os itens (arraste e solte).</td></tr></tbody></table>

#### Comportamento no formulário

* O respondente vê os itens como blocos repetíveis, cada um contendo todos os campos do formulário-template.
* Pode adicionar, remover, clonar e reordenar itens (conforme configuração).
* Na consulta, os dados são exibidos em formato de lista com as seções do formulário vinculado.
* Atributos condicionais (campo pai/filho) dentro do repeater funcionam normalmente, avaliando a condição no escopo de cada item individual.

#### Observações

* O formulário-template é vinculado por versão. Se você publicar uma nova versão do template, será necessário atualizar manualmente a versão no atributo Repeater para que novos preenchimentos utilizem a nova estrutura.
* Respostas já gravadas mantêm a estrutura da versão vigente no momento do preenchimento.
* Repeaters não podem ser aninhados (um repeater dentro de outro).
