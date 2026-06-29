# Formulários Externos

## Introdução

O SIAD permite transformar um tipo de atendimento em um **formulário público acessível sem login**, disponível por uma URL personalizada. Cada preenchimento gera automaticamente um registro de atendimento no sistema, vinculado a um equipamento e usuário padrão.

Essa funcionalidade é o precursor do SIAD Forms e foi amplamente utilizada em ações como o protocolo "Não Se Cale", ações de Carnaval e Virada Cultural — situações onde é necessário registrar ações de promoção e defesa de direitos humanos (distribuição de insumos, atendimentos técnicos em eventos) por pessoas que não possuem acesso ao sistema interno.

> **Nota sobre o futuro**: esta funcionalidade passará por uma revisão para ser integrada ao SIAD Forms, unificando a experiência de formulários públicos em uma única ferramenta. Os formulários externos existentes continuarão funcionando normalmente até a migração.

### Diferenças em relação ao SIAD Forms

| Aspecto                    | Formulário Externo de Atendimento               | SIAD Forms                                   |
| -------------------------- | ----------------------------------------------- | -------------------------------------------- |
| **Resultado**              | Gera um atendimento no módulo de Atendimento    | Gera um protocolo com respostas por etapa    |
| **Múltiplas etapas**       | Não — é um formulário único                     | Sim — suporta fluxos com múltiplas etapas    |
| **Versionamento**          | Não possui                                      | Formulários possuem versões publicadas       |
| **Acesso à configuração**  | Via cadastro de Tipo de Atendimento             | Via módulo de Formulários + Fluxos           |
| **Seções**                 | Definidas como tags no tipo de atendimento      | Definidas como registros separados na versão |
| **Integração com pessoas** | Opcional (campo Pessoa disponível internamente) | Via protocolo ou sem vínculo                 |
| **Consulta de protocolo**  | Por código de 8 caracteres do atendimento       | Por número de protocolo do fluxo             |

***

## Configurar o Tipo de Atendimento como Externo

A configuração é feita no cadastro de tipos de atendimentos. Acesse **Atendimento > Tipos de Atendimentos** e crie ou edite um tipo de atendimento.

### Dados Básicos

Na seção **Dados básicos**, configure:

<table><thead><tr><th width="191.666748046875">Campo</th><th width="126.6666259765625" align="center">Obrigatório</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Nome</strong></td><td align="center">Sim</td><td>Nome do tipo de atendimento. Será utilizado internamente para identificação.</td></tr><tr><td><strong>Grupo</strong></td><td align="center">Sim</td><td>Grupo de atendimento ao qual pertence (ex: "Promoção de Direitos", "Eventos").</td></tr><tr><td><strong>Descrição</strong></td><td align="center">Não</td><td>Texto descritivo sobre o tipo de atendimento.</td></tr><tr><td><strong>Data inicial</strong></td><td align="center">Sim</td><td>Data a partir da qual o formulário estará disponível. Se a data atual for anterior, o formulário será exibido como indisponível.</td></tr><tr><td><strong>Data final</strong></td><td align="center">Sim</td><td>Data até a qual o formulário estará disponível. Após essa data, novos registros não serão aceitos.</td></tr><tr><td><strong>Visibilidade</strong></td><td align="center">Sim</td><td>Selecione <strong>"Externo"</strong>. Essa é a opção que habilita o formulário público e exibe as configurações adicionais.</td></tr><tr><td><strong>Permitir sigilo?</strong></td><td align="center">Não</td><td>Quando ativado, permite marcar atendimentos como sigilosos.</td></tr><tr><td><strong>Prazo em dias para edição</strong></td><td align="center">Não</td><td>Limita o período para edição/exclusão de atendimentos após o registro.</td></tr></tbody></table>

> **Importante**: ao selecionar a visibilidade "Externo", uma nova seção chamada **"Configurações do formulário"** será exibida.

***

## Configurar o Formulário Público

A seção **Configurações do formulário** aparece somente quando a visibilidade é "Externo". Ela define toda a aparência e comportamento da página pública.

### Campos de identidade visual

<table><thead><tr><th width="163.6666259765625">Campo</th><th width="144.6666259765625" align="center">Obrigatório</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Título</strong></td><td align="center">Sim</td><td>Texto principal exibido no topo do formulário público. Ex: "Atendimento Virada Cultural 2025".</td></tr><tr><td><strong>Subtítulo</strong></td><td align="center">Não</td><td>Texto complementar exibido abaixo do título. Ex: "Registre o atendimento realizado no evento".</td></tr><tr><td><strong>Slug</strong></td><td align="center">Sim</td><td>Identificador usado na URL pública: <code>/public/{slug}</code>. Aceita apenas letras minúsculas, números e hífens. Ex: <code>virada-cultural-2025</code>. Deve ser único.</td></tr><tr><td><strong>Largura</strong></td><td align="center">Não</td><td>Largura máxima da página. Padrão: tela média.</td></tr><tr><td><strong>Instruções</strong></td><td align="center">Não</td><td>Bloco de texto rico exibido no formulário. Útil para orientações gerais ao preenchedor. Suporta formatação completa (negrito, listas, links, tabelas).</td></tr><tr><td><strong>Mensagem de sucesso</strong></td><td align="center">Não</td><td>Texto exibido após o registro bem-sucedido. Se vazio, exibe mensagem padrão.</td></tr></tbody></table>

### Banner

<table><thead><tr><th width="244">Campo</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Banner</strong></td><td>Upload de imagem exibida na página (logotipo, identidade visual do evento).</td></tr><tr><td><strong>Banner hook</strong></td><td>Posição de renderização do banner na página (topo, antes do conteúdo etc.). Padrão: início do conteúdo.</td></tr><tr><td><strong>Alinhamento do banner</strong></td><td>Esquerda, Centro, Direita ou Largura Total.</td></tr><tr><td><strong>Largura do banner (px)</strong></td><td>Largura em pixels quando o alinhamento não é "Largura Total". Padrão: 240px.</td></tr></tbody></table>

### Equipamento e Usuário padrão

Todo atendimento gerado pelo formulário público precisa estar vinculado a um equipamento e um usuário no sistema (campos obrigatórios do modelo de atendimento). Como o respondente não está logado, esses campos são definidos na configuração:

<table><thead><tr><th width="221.666748046875">Campo</th><th width="131.666748046875" align="center">Obrigatório</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Equipamento padrão</strong></td><td align="center">Sim</td><td>Equipamento que será vinculado a todos os atendimentos gerados por este formulário. Ex: "Coordenação de Políticas para LGBTI+".</td></tr><tr><td><strong>Usuário padrão</strong></td><td align="center">Sim</td><td>Usuário do equipamento selecionado que será registrado como autor do atendimento. Lista apenas profissionais ativos do equipamento.</td></tr></tbody></table>

### Outras configurações

<table><thead><tr><th width="230.6666259765625">Campo</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Ocultar data do atendimento</strong></td><td>Quando ativado, o campo de data/hora não é exibido ao respondente. A data atual é gravada automaticamente.</td></tr><tr><td><strong>Habilitar tela de acompanhamento?</strong></td><td>Quando ativado, disponibiliza um botão "Consultar Protocolo" que permite buscar e visualizar atendimentos já registrados informando o código de 8 caracteres.</td></tr></tbody></table>

***

## Configurar Seções e Atributos

Diferentemente do SIAD Forms (onde seções são entidades separadas), nos formulários externos de atendimento as seções são definidas como **tags** no próprio tipo de atendimento, e os atributos são vinculados a essas seções.

### Criar seções

Na seção **Controles de visibilidade** do tipo de atendimento, preencha o campo **Seções**:

* Digite o nome da seção e pressione **Enter** para adicionar
* Adicione quantas seções forem necessárias
* As seções podem ser reordenadas por arraste
* Ex: "Dados do Atendimento", "Identificação", "Descrição da Ocorrência"

Configure também o **Nº Colunas** (padrão: 3), que define o grid do formulário.

### Adicionar atributos

Após salvar o tipo de atendimento, acesse a aba **Atributos** na tela de edição (relation manager). Clique em **"Adicionar atributo"** para vincular campos ao formulário.

O formulário de adição de atributo contém:

<table><thead><tr><th width="210.3333740234375">Campo</th><th width="144" align="center">Obrigatório</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Atributo</strong></td><td align="center">Sim</td><td>Selecione um atributo existente ou crie um novo clicando em "+". Os atributos são os mesmos do SIAD Forms (Texto Curto, Lista, Data, CEP etc.).</td></tr><tr><td><strong>Seção</strong></td><td align="center">Sim</td><td>Selecione em qual seção o atributo será exibido (dentre as seções cadastradas).</td></tr><tr><td><strong>Ordem</strong></td><td align="center">Não</td><td>Posição numérica dentro da seção. Menor = mais acima.</td></tr><tr><td><strong>Chave Pai</strong></td><td align="center">Não</td><td>Informe a chave de outro atributo para criar dependência condicional.</td></tr><tr><td><strong>Opções Pai</strong></td><td align="center">Não</td><td>Se o campo pai for preenchido, informe quais valores acionam a exibição deste campo.</td></tr><tr><td><strong>Obrigatório?</strong></td><td align="center">Não</td><td>Torna o preenchimento obrigatório.</td></tr><tr><td><strong>Múltiplo?</strong></td><td align="center">Não</td><td>Permite seleção de múltiplos valores (para tipos que suportam).</td></tr><tr><td><strong>Largura total?</strong></td><td align="center">Não</td><td>O campo ocupa toda a largura disponível.</td></tr><tr><td><strong>Visibilidade na tabela?</strong></td><td align="center">Não</td><td>O valor aparece como coluna na listagem de atendimentos.</td></tr><tr><td><strong>Quebrar linha</strong></td><td align="center">Não</td><td>Força o campo a iniciar em nova linha.</td></tr><tr><td><strong>Ocultar externo</strong></td><td align="center">Não</td><td><strong>Específico para formulários externos.</strong> Quando ativado, o campo NÃO é exibido no formulário público — ele fica visível somente no modo de edição interna. Útil para campos que só fazem sentido para o técnico (ex: observações internas).</td></tr><tr><td><strong>Habilitar consulta externa</strong></td><td align="center">Não</td><td>Visível quando "Ocultar externo" está ativo. Permite que o campo seja exibido na tela de consulta por protocolo mesmo estando oculto no preenchimento.</td></tr></tbody></table>

### Campo Profissional

Na seção **Controles de visibilidade**, é possível configurar o campo "Profissional":

<table><thead><tr><th width="311.3333740234375">Campo</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Campo "Profissional" visível?</strong></td><td>Exibe um seletor de profissional do equipamento padrão no formulário.</td></tr><tr><td><strong>Campo "Profissional" múltiplo?</strong></td><td>Permite selecionar mais de um profissional.</td></tr><tr><td><strong>Campo "Profissional" obrigatório?</strong></td><td>Torna a seleção obrigatória.</td></tr></tbody></table>

Essa configuração é útil quando o evento tem múltiplos profissionais e o respondente precisa indicar quem realizou o atendimento.

### Campos de quantidade

<table><thead><tr><th width="299.3333740234375">Campo</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Campo "Quantidade" visível?</strong></td><td>Exibe campo de quantidade no formulário.</td></tr><tr><td><strong>Ocultar no formulário externo?</strong></td><td>Se ativo, o campo de quantidade fica visível somente na edição interna.</td></tr><tr><td><strong>Quantidade mínima / máxima</strong></td><td>Define limites de validação.</td></tr><tr><td><strong>Campo "Pessoas (Qtde)" visível?</strong></td><td>Exibe campo para informar total de pessoas participantes.</td></tr><tr><td><strong>Pessoas mínimo / máximo</strong></td><td>Define limites de validação para o campo de pessoas.</td></tr></tbody></table>

***

## URL Pública e Funcionamento

Após salvar todas as configurações, o formulário estará disponível em:

```
https://siad.prefeitura.sp.gov.br/public/{slug}
```

Na tela de edição do tipo de atendimento, ao lado do campo slug, há um botão de ícone (olho) que abre a URL em nova aba para visualização prévia.

### Fluxo do respondente

1. Acessa a URL pública
2. O sistema verifica se a data atual está entre `dt_inicio` e `dt_fim`
   * Se fora do período: exibe mensagem de "formulário indisponível"
   * Se dentro do período: renderiza o formulário
3. Preenche os campos obrigatórios e opcionais
4. Clica em **"Gravar"**
5. O sistema cria um atendimento vinculado ao equipamento e usuário padrão
6. Exibe a tela de sucesso com o **código do protocolo** (8 primeiros caracteres do UUID do atendimento)

### Consulta de protocolo

Se a opção **"Habilitar tela de acompanhamento"** estiver ativa, o formulário exibe um botão **"Consultar Protocolo"** no topo. Ao clicar:

1. O respondente informa os 8 caracteres do código recebido
2. O sistema busca o atendimento correspondente
3. Exibe os dados preenchidos em modo de leitura
4. Campos marcados com "Ocultar externo" (sem "Habilitar consulta externa") ficam ocultos
5. Campos com "Habilitar consulta externa" são exibidos mesmo estando ocultos no preenchimento

***

## Passo a Passo Resumido

Para colocar um formulário externo no ar:

1. Acessar **Atendimento > Tipos de Atendimentos > Criar**
2. Preencher nome, grupo, datas e selecionar visibilidade **"Externo"**
3. Configurar título, subtítulo, slug, banner, equipamento e usuário padrão
4. Definir as **seções** no campo de tags
5. Salvar o tipo de atendimento
6. Na aba **Atributos**, adicionar os campos do formulário vinculando-os às seções
7. Configurar obrigatoriedade, ordem, condicionais e demais opções
8. Testar a URL: `/public/{slug}`
9. Distribuir o link para os respondentes

***

## Considerações Importantes

* Cada formulário público preenchido gera **um atendimento** no sistema, vinculado ao equipamento e usuário padrão configurados.
* Os atendimentos gerados aparecem normalmente na listagem interna de atendimentos do equipamento, podendo ser editados, consultados e excluídos por técnicos com permissão.
* O campo **Pessoa** nunca é exibido no formulário externo por questões de segurança. Caso a visibilidade de pessoa esteja habilitada, ela aparecerá somente no modo de edição interna.
* Os mesmos atributos do SIAD Forms podem ser utilizados aqui (Texto Curto, Lista, Radio, CEP, Data etc.), pois o cadastro de atributos é compartilhado entre os módulos.
* Atributos marcados com "Ocultar externo" são uma ferramenta para separar campos de preenchimento público de campos de preenchimento interno, dentro do mesmo tipo de atendimento.
* A funcionalidade de **"Somar à quantidade"** permite que campos numéricos incrementem automaticamente o campo quantidade do atendimento (útil para contabilizar insumos distribuídos, por exemplo).
