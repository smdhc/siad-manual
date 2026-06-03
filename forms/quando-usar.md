# Quando usar?

## Visão geral

O SIAD possui três funcionalidades que utilizam formulários dinâmicos, cada uma com um propósito específico. Antes de iniciar a configuração de um novo formulário, é fundamental identificar qual delas se aplica ao caso em questão.

A escolha correta garante que os dados sejam armazenados no contexto adequado, com as integrações e regras de negócio apropriadas.

## As três funcionalidades

### SIAD Forms

Destinado a formulários de propósito geral que **não geram atendimentos** e **não estão vinculados a programas ou benefícios**. É a funcionalidade mais flexível e abrangente, voltada para processos administrativos, participativos e de planejamento.

**Use quando a demanda envolver:**

* Inscrições para conferências, eventos ou processos seletivos
* Eleições de conselhos e colegiados
* Planejamento orçamentário (PLOA, PPA)
* Editais de chamamento público
* Prestação de contas
* Relatórios de monitoramento
* Credenciamentos de entidades
* Pesquisas e levantamentos institucionais
* Solicitações diversas
* Qualquer processo que envolva etapas sequenciais (workflow) sem vínculo com atendimento ou benefício

### Formulário Externo de Atendimento

Destinado a formulários que **geram um registro de atendimento** no SIAD. Sempre que o preenchimento do formulário representar um atendimento consolidado realizado por um equipamento, esta é a funcionalidade correta.

**Use quando a demanda envolver:**

* Registro de atendimentos consolidados (sem vínculo com pessoa específica)
* Formulários que precisam alimentar os dados de atendimento de um equipamento
* Coletas de dados quantitativos sobre serviços prestados

**Exemplos:**

* Protocolo Não se Cale (Carnaval, Virada Cultural etc.)
* Contabilização de ações.

{% hint style="danger" %}
**Importante:** o formulário externo de atendimento não permite vinculação com pessoa cadastrada no sistema no momento de inserção. Essa restrição é intencional por questões de segurança, uma vez que o formulário é acessado externamente. Contudo, é possível vincular a uma pessoa manualmente após o registro, estando logado no sistema.
{% endhint %}

{% hint style="info" %}
**Nota:** futuramente, o SIAD Forms será aprimorado para unificar essas funcionalidades. Até lá, a distinção deve ser respeitada.
{% endhint %}

### SIAD Benefícios

Destinado a formulários vinculados a **programas da SMDHC** ou à concessão de **benefícios**. Também utiliza o construtor de formulários dinâmicos, mas opera em um contexto específico onde o formulário está obrigatoriamente vinculado a uma pessoa cadastrada no sistema.

**Use quando a demanda envolver:**

* Programas institucionais da SMDHC (Transcidadania, Cidade Solidária - Benefícios, etc.)
* Concessão, renovação ou acompanhamento de benefícios
* Qualquer processo em que o formulário precise estar vinculado a uma pessoa

**Exemplos:**

* Auxílio Aluguel
* Auxílio Ampara
* POTs.

## Resumo comparativo

| Critério                                 | SIAD Forms                                          | Formulário Externo de Atendimento | SIAD Benefícios                 |
| ---------------------------------------- | --------------------------------------------------- | --------------------------------- | ------------------------------- |
| **Gera atendimento?**                    | Não                                                 | Sim                               | Não                             |
| **Vinculado a pessoa?**                  | Não (opcional)                                      | Não (somente na edição)           | Sim (obrigatório)               |
| **Vinculado a programa/benefício?**      | Não                                                 | Não                               | Sim                             |
| **Suporta workflow (múltiplas etapas)?** | Sim                                                 | Não                               | Não                             |
| **Acesso público (sem login)?**          | Sim                                                 | Sim                               | Não                             |
| **Exemplo típico**                       | Inscrição em conferência, eleição de conselho, PLOA | Protocolo não se cale             | Transcidadania, auxílio-aluguel |

## Fluxo de decisão

Para identificar rapidamente a funcionalidade correta, siga este raciocínio:

1. **O formulário vai gerar um atendimento?**
   * Sim → **Formulário Externo de Atendimento**
2. **O formulário está vinculado a um programa da SMDHC ou à concessão de um benefício?**
   * Sim → **SIAD Benefícios**
3. **Nenhuma das anteriores?**
   * → **SIAD Forms**

## Em caso de dúvida

Sempre que houver incerteza sobre qual funcionalidade utilizar, ou quando a demanda parecer se enquadrar em mais de uma categoria, **consulte a equipe da CPI antes de iniciar qualquer configuração**. A escolha equivocada da funcionalidade pode implicar retrabalho significativo e impactar a integridade dos dados.
