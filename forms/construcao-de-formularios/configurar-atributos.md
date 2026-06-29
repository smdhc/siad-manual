# Configurar atributos

## Acessando a listagem de atributos

Para acessar a tela de configuração dos atributos da seção, a partir da listagem das seções, clique na coluna "# Atributos" ou no item de menu "Atributos", no ícone de opções da seção desejada.

<figure><img src="../../.gitbook/assets/image (89).png" alt=""><figcaption></figcaption></figure>

Ao fazer isso, você será redirecionado para a listagem de atributos daquela seção.

<figure><img src="../../.gitbook/assets/image (90).png" alt=""><figcaption></figcaption></figure>

## Adicionar atributos

Para começar a adicionar atributos para a seção, basta clicar no botão "Adicionar Atributo". Será aberta uma janela para selecionar um atributo já existente ou criar um novo.

{% hint style="info" %}
Todos os atributos criados podem ser reutilizados em formulários distintos. Contudo, recomendamos sempre criar novos atributos para evitar conflito com outros formulários.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (96).png" alt=""><figcaption></figcaption></figure>

## Criando novos atributos

Atributos são os campos propriamente ditos que compõem um formulário. Cada atributo representa uma pergunta ou dado a ser coletado na seção em que está inserido.

Nesse exemplo, iremos criar um novo atributo que irá coletar o "Nome da pessoa". Para isso, clique no botão "+" localizado no canto direito do Atributo, conforme imagem abaixo. Será aberta então uma janela para cadastrar os dados gerais desse atributo.

<figure><img src="../../.gitbook/assets/image (100).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (104).png" alt=""><figcaption></figcaption></figure>

### Campos comuns a todos os atributos

<table><thead><tr><th width="140.333251953125">Campo</th><th width="125.666748046875" align="center">Obrigatório</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Label</strong></td><td align="center">Sim</td><td>O rótulo que será exibido para o respondente do formulário. Ex: "Nome da pessoa".</td></tr><tr><td><strong>Chave</strong></td><td align="center">Sim</td><td>Identificador único do atributo, gerado automaticamente a partir da label (slug + sufixo aleatório). Utilizado para referenciar o atributo em regras, condicionais e integrações. Aceita apenas letras minúsculas, números, hífens e underscores. Não pode ser alterada após a criação.</td></tr><tr><td><strong>Tipo</strong></td><td align="center">Sim</td><td>Define o comportamento e a aparência do campo no formulário. Veja a seção "Tipos de Atributo" abaixo.</td></tr><tr><td><strong>Placeholder</strong></td><td align="center">Não</td><td>Texto exibido dentro do campo quando ele está vazio, servindo como dica de preenchimento. Oculto para tipos que não utilizam entrada de texto (ex: Markdown, Imagem).</td></tr><tr><td><strong>Helper Text</strong></td><td align="center">Não</td><td>Texto de ajuda exibido abaixo do campo. Útil para orientar o preenchimento com instruções ou exemplos.</td></tr><tr><td><strong>Conteúdo extra</strong></td><td align="center">Não</td><td>Permite inserir conteúdo HTML adicional em posições específicas ao redor do campo (acima/abaixo da label, antes/depois do conteúdo etc.). Cada item requer a seleção da posição e o conteúdo a ser exibido.</td></tr></tbody></table>

### Campos específicos do tipo Texto Curto

Ao selecionar o tipo **Texto Curto**, dois campos adicionais aparecem:

<table><thead><tr><th width="250.6666259765625">Campo</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Tamanho Mínimo do Texto</strong></td><td>Quantidade mínima de caracteres aceita. Ex: 3</td></tr><tr><td><strong>Tamanho Máximo do Texto</strong></td><td>Quantidade máxima de caracteres permitida. Ex: 70</td></tr><tr><td><strong>Máscara</strong></td><td>Padrão de formatação visual para a digitação. Ex: <code>(99) 99999-9999</code> para telefone.</td></tr><tr><td><strong>Expressão Regular</strong></td><td>Regex de validação customizada para o campo. Ex: <code>/^.+@.+$/i</code> para validar formato de e-mail.</td></tr></tbody></table>

### Exemplo prático: criando o campo "Nome da pessoa"

1. No campo **Label**, digite: `Nome da pessoa`
2. A **Chave** será preenchida automaticamente como algo similar a `nome_da_pessoa_3eab`
3. No campo **Tipo**, selecione: `Texto Curto`
4. Deixe o **Placeholder** em branco (ou preencha com algo como "Digite o nome completo")
5. Deixe o **Helper Text** em branco (ou adicione uma orientação como "Informe o nome civil completo")
6. Em **Tamanho Mínimo do Texto**, informe: `3`
7. Em **Tamanho Máximo do Texto**, informe: `70`
8. Deixe **Máscara** e **Expressão Regular** em branco (não se aplicam para nome)
9. Clique em **Criar**

O atributo será criado e passará a estar disponível para ser vinculado a seções de formulários.

***

## Tipos de Atributo disponíveis

A tabela abaixo lista todos os tipos de atributo suportados pelo SIAD Forms, com uma breve descrição de cada um:

<table><thead><tr><th width="174.6666259765625">Tipo</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Texto Curto</strong></td><td>Campo de texto simples, ideal para nomes, títulos e informações breves. Permite configurar tamanho mínimo/máximo, máscara e regex.</td></tr><tr><td><strong>Texto Longo</strong></td><td>Área de texto multi-linha para descrições, observações e textos extensos. Permite configurar tamanho mínimo/máximo.</td></tr><tr><td><strong>Inteiro</strong></td><td>Campo numérico que aceita apenas números inteiros. Permite configurar valor mínimo e máximo.</td></tr><tr><td><strong>Decimal</strong></td><td>Campo numérico que aceita casas decimais. Permite configurar valor mínimo e máximo.</td></tr><tr><td><strong>Moeda</strong></td><td>Campo numérico formatado como valor monetário (R$). Permite configurar valor mínimo e máximo.</td></tr><tr><td><strong>Data</strong></td><td>Seletor de data (dia/mês/ano).</td></tr><tr><td><strong>Data/Hora</strong></td><td>Seletor de data e hora.</td></tr><tr><td><strong>E-mail</strong></td><td>Campo de texto com validação de formato de e-mail.</td></tr><tr><td><strong>CPF</strong></td><td>Campo com máscara e validação de CPF.</td></tr><tr><td><strong>CNPJ</strong></td><td>Campo com máscara e validação de CNPJ.</td></tr><tr><td><strong>CEP</strong></td><td>Campo com máscara de CEP e possibilidade de consulta de endereço.</td></tr><tr><td><strong>Checkbox</strong></td><td>Caixa de seleção (sim/não).</td></tr><tr><td><strong>Toggle</strong></td><td>Interruptor liga/desliga, similar ao Checkbox mas com visual diferente.</td></tr><tr><td><strong>Lista</strong></td><td>Seleção única ou múltipla a partir de opções fixas definidas manualmente no cadastro do atributo.</td></tr><tr><td><strong>Lista Dinâmica</strong></td><td>Similar à Lista, mas com opções dinâmicas.</td></tr><tr><td><strong>Radio</strong></td><td>Seleção única com botões radio a partir de opções fixas.</td></tr><tr><td><strong>Radio Dinâmico</strong></td><td>Similar ao Radio, mas com opções dinâmicas.</td></tr><tr><td><strong>Arquivo</strong></td><td>Upload de arquivos. Permite configurar o diretório de armazenamento e tamanho máximo.</td></tr><tr><td><strong>Imagem</strong></td><td>Upload ou URL de imagem, com texto alternativo para acessibilidade.</td></tr><tr><td><strong>Markdown</strong></td><td>Bloco de conteúdo rico (texto formatado), usado para inserir instruções, avisos ou informações dentro do formulário. Não coleta dados.</td></tr><tr><td><strong>SEI</strong></td><td>Campo para número de processo SEI.</td></tr><tr><td><strong>Pessoa</strong></td><td>Seletor de pessoa cadastrada no sistema (integração com cadastro de pessoas do SIAD).</td></tr><tr><td><strong>Profissional</strong></td><td>Seletor de profissional/usuário do sistema.</td></tr><tr><td><strong>Organização</strong></td><td>Seletor de organização cadastrada no SIAD.</td></tr><tr><td><strong>Equipamentos</strong></td><td>Seletor de equipamento(s) cadastrados no SIAD. Permite filtrar por temática e tipo de equipamento.</td></tr><tr><td><strong>Equipamento Logado</strong></td><td>Captura automaticamente o equipamento vinculado ao usuário logado.</td></tr><tr><td><strong>Usuário Logado</strong></td><td>Captura automaticamente o usuário que está preenchendo o formulário.</td></tr><tr><td><strong>Município</strong></td><td>Seletor de município.</td></tr><tr><td><strong>UF</strong></td><td>Seletor de unidade federativa.</td></tr><tr><td><strong>País</strong></td><td>Seletor de país.</td></tr><tr><td><strong>Distrito</strong></td><td>Seletor de distrito (região administrativa).</td></tr><tr><td><strong>Subprefeitura</strong></td><td>Seletor de subprefeitura.</td></tr><tr><td><strong>Raça/Cor</strong></td><td>Seletor com as opções padronizadas de raça/cor.</td></tr><tr><td><strong>Identidade de Gênero</strong></td><td>Seletor com as opções padronizadas de identidade de gênero.</td></tr><tr><td><strong>Orientação Sexual</strong></td><td>Seletor com as opções padronizadas de orientação sexual.</td></tr><tr><td><strong>Condição de Moradia</strong></td><td>Seletor com as opções padronizadas de condição de moradia.</td></tr><tr><td><strong>Escolaridade</strong></td><td>Seletor com os níveis de escolaridade.</td></tr><tr><td><strong>Tipo de Deficiência</strong></td><td>Seletor com os tipos de deficiência.</td></tr><tr><td><strong>Situação Migratória</strong></td><td>Seletor com as opções de situação migratória (chave fixa: <code>situacao_migratoria</code>).</td></tr><tr><td><strong>Menor Desacompanhado</strong></td><td>Campo booleano (Sim/Não) para indicar se é menor desacompanhado (chave fixa: <code>menor_desacompanhado</code>).</td></tr><tr><td><strong>Pontuação</strong></td><td>Campo especial para sistemas de pontuação. Permite configurar o tipo de agregação (soma ou média ponderada).</td></tr><tr><td><strong>Resultado</strong></td><td>Campo que exibe o resultado calculado a partir de atributos do tipo Pontuação.</td></tr><tr><td><strong>Repeater</strong></td><td>Campo agrupador que permite repetir um conjunto de campos (baseado em uma versão publicada de outro formulário).</td></tr></tbody></table>

### Observações sobre os tipos

* Tipos como **Pessoa**, **Profissional**, **Organização** e **Equipamentos** fazem integração direta com outros módulos do SIAD.
* Tipos como **Raça/Cor**, **Identidade de Gênero**, **Orientação Sexual**, **Condição de Moradia**, **Escolaridade** e **Tipo de Deficiência** utilizam enumerações padronizadas do sistema — não é necessário definir as opções manualmente.
* Os tipos **Equipamento Logado** e **Usuário Logado** são preenchidos automaticamente e não exibem placeholder nem helper text.
* O tipo **Markdown** não coleta dados do respondente; serve exclusivamente para exibir conteúdo informativo no formulário.
* Os tipos **Lista**, **Lista Dinâmica**, **Radio** e **Radio Dinâmico** exigem a configuração de opções no momento da criação do atributo.

***

## Configurar atributo na seção

Após criar o atributo, o sistema exibirá novamente a janela **"Adicionar Atributo à Seção"**, com o atributo recém-criado já selecionado no campo **Atributo** e as demais opções de configuração disponíveis para definir como o campo se comportará dentro daquela seção específica.

Essa configuração é independente do atributo em si — ou seja, o mesmo atributo pode ser utilizado em seções ou formulários diferentes com configurações distintas (obrigatoriedade, largura, visibilidade etc.).

### Campos de configuração

<table><thead><tr><th width="198">Campo</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Atributo</strong></td><td>Campo obrigatório. Exibe o atributo selecionado no formato <code>Label (chave) - Tipo</code>. Caso deseje criar um novo atributo diretamente por aqui, basta clicar no botão <strong>+</strong> ao lado do campo.</td></tr><tr><td><strong>Ordem</strong></td><td>Número inteiro que define a posição do atributo dentro da seção. Quanto menor o número, mais acima ele aparecerá. Valor padrão: <code>0</code>.</td></tr><tr><td><strong>Chave Pai</strong></td><td>Permite vincular o atributo a um campo "pai". Quando preenchido, o atributo só será exibido no formulário se o campo pai possuir determinado valor selecionado. Somente atributos elegíveis como pai são listados (ex: Lista, Radio, Checkbox de categorias etc.).</td></tr><tr><td><strong>Opções Pai</strong></td><td>Visível apenas quando uma Chave Pai está selecionada. Permite escolher quais valores do campo pai funcionarão como gatilho para exibir este atributo.</td></tr><tr><td><strong>Obrigatório exceto se o campo for</strong></td><td>Informe a chave de outro atributo. O campo atual será obrigatório a menos que o atributo referenciado contenha o valor especificado no campo ao lado.</td></tr><tr><td><strong>Obrigatório exceto se o valor for</strong></td><td>Complementa o campo anterior. Informe o valor que, quando presente no atributo referenciado, tornará o preenchimento deste campo dispensável.</td></tr><tr><td><strong>Nº colunas</strong></td><td>Define quantas colunas do grid o atributo ocupará no formulário. O layout padrão do formulário possui 2 colunas. Não é exibido quando "Ocupar largura total" está ativo.</td></tr></tbody></table>

### Toggles de comportamento

<table><thead><tr><th width="226">Toggle</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Obrigatório?</strong></td><td>Quando ativado, o respondente será obrigado a preencher este campo para submeter o formulário. Oculto para tipos que não aceitam preenchimento direto (Markdown, Imagem, Usuário Logado, Equipamento Logado, Repeater).</td></tr><tr><td><strong>Ocupar largura total?</strong></td><td>Quando ativado, o atributo ocupará toda a largura disponível (as 2 colunas), ignorando o campo "Nº colunas".</td></tr><tr><td><strong>Visibilidade na tabela?</strong></td><td>Quando ativado, o valor deste atributo será exibido como coluna na tabela de respostas/atendimentos. Disponível apenas para tipos cujos valores fazem sentido em formato tabular.</td></tr><tr><td><strong>Quebrar linha</strong></td><td>Quando ativado, força uma quebra de linha antes deste campo, garantindo que ele inicie em uma nova linha no formulário.</td></tr><tr><td><strong>Único</strong></td><td>Quando habilitado, o sistema impede a submissão de formulários com valor duplicado neste atributo para a mesma etapa. Útil para campos como CPF, e-mail ou qualquer dado que não deva se repetir.</td></tr></tbody></table>

### Configurações de Acesso

Permite definir permissões granulares por perfil de usuário. Clique em **"Adicionar regra"** para configurar uma regra de acesso.

Cada regra contém:

* **Perfil**: o papel do usuário (Editor ou Usuário)
* **Permissão**: as ações permitidas para aquele perfil (Consultar, Cadastrar, Alterar)

Caso nenhuma regra seja configurada, todos os perfis poderão consultar, cadastrar e alterar o campo livremente.

#### Toggle final

<table><thead><tr><th width="151.3333740234375">Toggle</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Desabilitado?</strong></td><td>Quando ativado, o campo será exibido no formulário em modo somente leitura (o respondente poderá visualizá-lo, mas não editá-lo). Disponível para tipos como Texto Curto, Texto Longo, Inteiro, Decimal, Moeda, E-mail, Data, Data/Hora e CPF.</td></tr></tbody></table>

### Botões de ação

* **Criar**: salva a configuração do atributo na seção e fecha o modal.
* **Salvar e criar outro**: salva a configuração e reabre o modal limpo para adicionar mais um atributo na mesma seção.
* **Cancelar**: descarta as alterações e fecha o modal.

### Campos adicionais condicionais

Dependendo do tipo de atributo selecionado, campos extras podem ser exibidos:

<table><thead><tr><th width="238.6666259765625">Condição</th><th>Campos adicionais</th></tr></thead><tbody><tr><td>Tipo = Lista, Radio (e variantes dinâmicas)</td><td><strong>Ordenação</strong> (Nenhuma, Ascendente, Descendente) para ordenar as opções exibidas. Opção de configurar <strong>Pontuação</strong> com mapa de valores.</td></tr><tr><td>Tipo = Inteiro, Decimal ou Moeda</td><td><strong>Valor padrão</strong>, validações numéricas (Maior que, Maior ou igual a, Menor que, Menor ou igual a) referenciando chaves de outros atributos.</td></tr><tr><td>Tipo = Data ou Data/Hora</td><td><strong>Validações de Data</strong> — regras temporais com operadores (antes de, depois de, igual a etc.) comparando com outro atributo, data fixa ou data relativa (ex: +30 days).</td></tr><tr><td>Tipo = CEP</td><td>Mapeamento de campos para preenchimento automático (Logradouro, Bairro, Município, Distrito, UF).</td></tr><tr><td>Tipo = CNPJ</td><td>Mapeamento de campos para preenchimento automático (Razão Social, Nome Fantasia, E-mail, Telefone, CEP, Logradouro, Número, Complemento, Bairro, Nome do Responsável, E-mail do Responsável).</td></tr><tr><td>Tipo = Imagem</td><td>Configurações de <strong>Alinhamento</strong>, <strong>Largura</strong> e <strong>Altura</strong> da imagem no formulário.</td></tr><tr><td>Tipo = Repeater</td><td>Quantidade padrão de itens, mínimo/máximo de itens, label do botão adicionar, e opção de bloquear reordenamento.</td></tr><tr><td>Tipo = Resultado</td><td>Seleção do atributo de Pontuação vinculado e configuração das faixas de resultado (mínimo, máximo, label).</td></tr><tr><td>Tipo aceita múltiplo (Lista, Equipamentos, Pessoa etc.)</td><td><strong>Múltiplo?</strong> — permite selecionar mais de um valor.</td></tr><tr><td>Tipo = Radio</td><td><strong>Inline?</strong> — exibe as opções na horizontal.</td></tr><tr><td>Tipo = Inteiro</td><td><strong>Somar à quantidade?</strong> — soma o valor ao total quantitativo do registro.</td></tr></tbody></table>

## Finalizando criação do atributo

No nosso exemplo, vou definir o campo "Nome da pessoa" com ordem = 1, para ser o primeiro atributo da seção, obrigatório e ocupando a largura total da tela (que foi configurada com 2 colunas na seção).

<figure><img src="../../.gitbook/assets/image (108).png" alt=""><figcaption></figcaption></figure>

Clique em "Criar" para finalizar a configuração. A listagem de atributos será atualizada com o atributo novo.

<figure><img src="../../.gitbook/assets/image (118).png" alt=""><figcaption></figcaption></figure>
