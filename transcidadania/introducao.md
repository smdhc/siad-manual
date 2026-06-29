# Introdução

## Introdução ao Programa Transcidadania

O módulo **Transcidadania** no SIAD é dedicado à gestão do Programa Transcidadania — programa da Prefeitura de São Paulo voltado à promoção da cidadania e inclusão social de pessoas trans (mulheres transexuais e homens trans), por meio de ações integradas de educação, qualificação profissional e promoção de direitos humanos.

O módulo permite cadastrar as pessoas beneficiárias, acompanhar mensalmente suas frequências escolares e em atividades complementares, calcular automaticamente os descontos e valores de pagamento do benefício, e registrar o Plano Individual de Atendimento (PIA).

***

### Público-alvo do programa

O Programa Transcidadania é voltado exclusivamente para **pessoas trans** — mulheres transexuais e homens trans. O sistema valida a elegibilidade automaticamente a partir da identidade de gênero registrada no cadastro da pessoa. Pessoas cuja identidade de gênero não se enquadre no perfil elegível não podem ser cadastradas no programa.

***

### Hierarquia do módulo

```
Transcidadania
├── Cadastro (vínculo da pessoa ao programa)
│   ├── Dados do programa (status, equipamento, datas, escola, documentos)
│   ├── Acompanhamento Mensal (frequências)
│   │   ├── Frequência escolar (%)
│   │   ├── Frequência em atividades complementares (%)
│   │   ├── Cálculo automático de desconto e pagamento
│   │   └── Comprovantes (uploads)
│   └── PIA — Plano Individual de Atendimento
│       ├── Múltiplos formulários configuráveis
│       ├── Registro por beneficiário
│       └── Histórico de alterações campo-a-campo
└── Configurações (administrador)
    ├── Janelas de preenchimento de frequência
    ├── Valores anuais do benefício
    └── Formulários do PIA
```

***

### Status no programa

As pessoas cadastradas no Transcidadania podem assumir os seguintes status:

<table><thead><tr><th width="224.666748046875">Status</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Ativo</strong></td><td>Pessoa inserida e participando do programa. Gera obrigatoriedade de acompanhamento mensal e pagamento do benefício.</td></tr><tr><td><strong>Inativo</strong></td><td>Pessoa desligada do programa. Requer data e motivo de desligamento.</td></tr><tr><td><strong>Suspenso</strong></td><td>Pessoa aguardando término de estágio probatório de emprego para desligamento. Limite de 90 dias — após esse prazo, gera alerta de inconsistência.</td></tr><tr><td><strong>Fila de Espera (Ativo)</strong></td><td>Pessoa aguardando vaga para ser inserida no programa.</td></tr><tr><td><strong>Fila de Espera (Inativo)</strong></td><td>Pessoa que foi removida da fila de espera (com data e motivo de saída da fila).</td></tr></tbody></table>

#### Transições de status permitidas

As transições não são livres — cada status só pode avançar para determinados destinos:

<table><thead><tr><th width="245.3333740234375">Status atual</th><th>Pode mudar para</th></tr></thead><tbody><tr><td>Ativo</td><td>Inativo, Suspenso</td></tr><tr><td>Inativo</td><td>Ativo, Fila de Espera (Ativo)</td></tr><tr><td>Suspenso</td><td>Ativo, Inativo</td></tr><tr><td>Fila de Espera (Ativo)</td><td>Ativo, Fila de Espera (Inativo)</td></tr><tr><td>Fila de Espera (Inativo)</td><td>Ativo, Fila de Espera (Ativo)</td></tr></tbody></table>

***

### Funcionalidades principais

#### Cadastro no programa

Formulário de inserção que registra o vínculo da pessoa com o programa, incluindo:

* Perfil da pessoa beneficiária (vinculação, área de interesse profissional)
* Dados educacionais (escolaridade, elevação escolar, rede escolar, escola)
* Dados do programa (status, data de inserção, código de benefício, agência bancária, documentos)

#### Acompanhamento mensal (frequências)

Registro periódico (mensal) das frequências de cada pessoa ativa no programa:

* Frequência escolar (peso de 60%)
* Frequência em atividades complementares (peso de 40%)
* Cálculo automático da frequência total e faixa de desconto
* Cálculo automático do valor de pagamento
* Controle de janelas de preenchimento (prazos configuráveis)
* Gestão de pendências (quem ainda não teve frequência registrada no mês)

#### PIA — Plano Individual de Atendimento

Conjunto de formulários dinâmicos que documentam o planejamento e evolução individual de cada pessoa no programa:

* Múltiplos formulários configuráveis pelo administrador
* Sinalização de status (preenchido, desatualizado, pendente)
* Histórico detalhado de alterações campo-a-campo
* Impressão individual ou em lote

#### Painel de acompanhamento

Visão gerencial que permite ao técnico ou coordenador verificar rapidamente:

* Frequências já registradas no mês
* Beneficiários pendentes de registro
* Informações das janelas de preenchimento (datas, status)

***

### Integração com o cadastro de pessoas

O Transcidadania é integrado nativamente ao cadastro de pessoas do SIAD:

* Toda pessoa cadastrada no programa deve existir previamente como pessoa no SIAD
* A aba **"Transcidadania"** aparece na sidebar do perfil da pessoa (quando o módulo está habilitado no equipamento do usuário)
* A escolaridade registrada no Transcidadania é sincronizada automaticamente com o cadastro geral da pessoa
* O benefício "Transcidadania" é adicionado/removido automaticamente do cadastro da pessoa conforme o status no programa
* Alertas de inconsistência de identidade de gênero são gerados automaticamente quando há alterações incompatíveis

***

### Pré-requisitos para acesso ao módulo

Para que um usuário consiga acessar o módulo Transcidadania, **duas condições** devem ser atendidas simultaneamente:

1. **Permissão de acesso**: o usuário deve possuir a permissão `TRANSCIDADANIA_ACESSAR`
2. **Módulo habilitado no equipamento**: o equipamento ao qual o usuário está vinculado deve ter o módulo Transcidadania habilitado em suas configurações

Quando ambas as condições são satisfeitas, o usuário passa a visualizar:

* Os menus **Transcidadania > Cadastro** e **Transcidadania > Acompanhamento** no módulo de Atendimento
* A aba **"Transcidadania"** no perfil das pessoas (sidebar)

***

### Alertas de inconsistência

O sistema identifica automaticamente situações que requerem atenção e sinaliza visualmente (fundo vermelho na listagem):

<table><thead><tr><th width="308.6666259765625">Inconsistência</th><th>Condição</th></tr></thead><tbody><tr><td>Identidade de gênero incompatível</td><td>A identidade de gênero registrada não é de pessoa trans</td></tr><tr><td>Suspensão acima do permitido</td><td>Status "Suspenso" por mais de 90 dias</td></tr><tr><td>Excesso de faltas</td><td>3 ou mais meses com frequência "NÃO PAGAR" ou "POSSIBILIDADE DE DESLIGAMENTO" nos últimos 12 meses</td></tr><tr><td>Escola divergente</td><td>Nome da escola no cadastro difere da escola informada na última frequência</td></tr></tbody></table>

Esses alertas são informativos e não impedem a operação — servem como sinalização para os técnicos tomarem providências.

***

### Navegação no sistema

O módulo Transcidadania é acessado pelos seguintes caminhos:

<table><thead><tr><th width="324">Menu</th><th>Funcionalidade</th></tr></thead><tbody><tr><td><strong>Transcidadania > Cadastro</strong></td><td>Listagem e gestão dos cadastros no programa</td></tr><tr><td><strong>Transcidadania > Acompanhamento</strong></td><td>Painel gerencial de frequências (registradas e pendentes)</td></tr><tr><td><strong>Transcidadania > Configurações</strong></td><td>Configurações administrativas (janelas, valores, PIA) — apenas administradores</td></tr><tr><td><strong>Pessoa > aba Transcidadania</strong></td><td>Visão consolidada do programa dentro do perfil da pessoa (cadastro + PIA + frequências)</td></tr></tbody></table>
