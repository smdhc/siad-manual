# Parte III — Regras de Negócio

## Regras de Inconsistência

O sistema identifica automaticamente situações que requerem atenção por parte dos técnicos e coordenadores. Quando uma inconsistência é detectada, o cadastro aparece com **fundo vermelho** na listagem e os detalhes são exibidos como alertas.

### Inconsistência 1 — Identidade de gênero incompatível

O Programa Transcidadania é voltado exclusivamente para pessoas trans. O sistema sinaliza inconsistência quando a identidade de gênero registrada no cadastro da pessoa é alterada para um valor incompatível com o perfil do programa.

**Quando é detectada:**

* A identidade de gênero da pessoa é alterada no cadastro geral (módulo Atendimento) para um valor que não se enquadra como pessoa trans

**Quando é removida:**

* A identidade de gênero é corrigida para um valor compatível com o perfil trans

**Implicação prática:** pode indicar erro de preenchimento no cadastro da pessoa ou necessidade de reavaliação do vínculo com o programa.

### Inconsistência 2 — Período de suspensão acima do permitido

Pessoas com status "Suspenso" possuem um limite máximo de **90 dias** nessa condição. Quando esse prazo é ultrapassado, o sistema gera alerta.

**Quando é detectada:**

* Status = "Suspenso" E a data de início da suspensão está há mais de 90 dias

**Quando é removida:**

* O status é alterado para Ativo ou Inativo (resolvendo a suspensão)

**Implicação prática:** indica que a situação de suspensão precisa ser resolvida — ou a pessoa retorna ao programa (Ativo) ou é desligada (Inativo).

### Inconsistência 3 — Excesso de faltas no período

O sistema contabiliza os meses de frequência classificados como **"NÃO PAGAR"** ou **"POSSIBILIDADE DE DESLIGAMENTO"** dentro de um intervalo configurável (padrão: 12 meses). Quando a pessoa acumula 3 ou mais meses nessa condição, o alerta é emitido.

**Quando é detectada:**

* 3 ou mais registros de frequência com desconto "NÃO PAGAR" ou "POSSIBILIDADE DE DESLIGAMENTO" dentro do intervalo configurado
* Somente frequências de cadastros com status "Ativo" são contabilizadas

**Quando é removida:**

* O número de meses com baixa frequência no intervalo volta a ser inferior a 3 (conforme o tempo passa e meses antigos saem do intervalo)

**Configuração:** o intervalo de meses considerado é configurável pelo administrador no campo "Período em meses para identificar inconsistência" (padrão: 12 meses).

### Inconsistência 4 — Escola divergente

O sistema alerta quando o nome da escola registrada no cadastro do Transcidadania **difere** do nome da escola informada na frequência mais recente.

**Quando é detectada:**

* O campo escola no cadastro possui um valor diferente do campo escola na última frequência registrada

**Quando é removida:**

* O cadastro é atualizado com a escola correta, ou uma nova frequência é registrada com a mesma escola do cadastro

**Por que acontece:** a sincronização entre frequência e cadastro ocorre apenas no **registro** de uma nova frequência (não na edição). Se o técnico registrou a frequência com dados errados e depois corrigiu via edição, o cadastro não será atualizado automaticamente. A inconsistência serve como alerta para o técnico corrigir manualmente o cadastro.

***

## Regras de Sincronização

O módulo Transcidadania mantém três camadas de dados sincronizadas automaticamente: o **Cadastro da Pessoa** (dados gerais no SIAD), o **Cadastro do Transcidadania** (dados do programa) e o **Acompanhamento Mensal** (frequências).

### Ao registrar uma nova frequência

#### Limpeza automática do nome da escola

Quando a rede escolar informada na frequência for **Estadual** ou **Municipal**, o campo de nome da escola personalizado (digitado manualmente) é automaticamente apagado. Nesses casos, o sistema usa a escola vinculada à lista oficial.

#### Sincronização com o cadastro do programa

No momento em que uma **nova** frequência é registrada (não se aplica a edições posteriores), o sistema verifica se ela é referente ao mês atual ou ao mês imediatamente anterior. Se for, os seguintes dados são copiados automaticamente para o Cadastro do Transcidadania:

<table><thead><tr><th width="260.666748046875">Dado sincronizado</th><th>Descrição</th></tr></thead><tbody><tr><td>Status</td><td>Status informado na frequência (Ativo, Inativo, Suspenso)</td></tr><tr><td>Motivo de desligamento</td><td>Se aplicável</td></tr><tr><td>Data de desligamento</td><td>Se aplicável</td></tr><tr><td>Rede escolar</td><td>Rede informada na frequência</td></tr><tr><td>Escola vinculada</td><td>Escola selecionada (ID)</td></tr><tr><td>Nome da escola</td><td>Nome digitado (para redes Particular/Outra)</td></tr><tr><td>Elevação escolar</td><td>Nível escolar atual</td></tr></tbody></table>

> **Regra fundamental**: a sincronização ocorre **apenas no ato do registro**, nunca na edição. Frequências corrigidas posteriormente via edição não atualizam o cadastro principal. Divergências geradas por essa situação são sinalizadas pela inconsistência de escola (Regra 4).

### Ao salvar o cadastro do Transcidadania

#### Sincronização da escolaridade com o cadastro da pessoa

Quando a escolaridade informada no cadastro do Transcidadania for diferente da registrada no cadastro geral da pessoa, o sistema atualiza automaticamente a pessoa com o novo valor.

| Origem                                 | Destino                           | Condição                    |
| -------------------------------------- | --------------------------------- | --------------------------- |
| Cadastro Transcidadania → Escolaridade | Cadastro da Pessoa → Escolaridade | Somente se forem diferentes |

#### Sincronização do benefício "Transcidadania"

| Situação                                  | Ação automática                                                                 |
| ----------------------------------------- | ------------------------------------------------------------------------------- |
| Status alterado para **Ativo**            | Benefício "Transcidadania" é **adicionado** ao cadastro de benefícios da pessoa |
| Status alterado para qualquer outro valor | Benefício "Transcidadania" é **removido** do cadastro da pessoa                 |

#### Preenchimento automático da saída da fila

Quando uma pessoa transita de **"Fila de Espera (Ativo)"** para **"Ativo"** e ainda não possui data nem motivo de saída da fila registrados:

| Campo preenchido automaticamente | Valor                                |
| -------------------------------- | ------------------------------------ |
| Data de saída da fila            | Igual à data de inserção no programa |
| Motivo de saída da fila          | "Inserção no Programa"               |

### Ao salvar o cadastro da pessoa

#### Verificação de consistência de identidade de gênero

Sempre que os dados de uma pessoa são salvos no módulo de Atendimento, o sistema verifica se a identidade de gênero é compatível com o programa:

| Situação                                                                | Ação automática                                     |
| ----------------------------------------------------------------------- | --------------------------------------------------- |
| Pessoa cadastrada no Transcidadania + identidade de gênero incompatível | Cadastro do programa marcado como **inconsistente** |
| Identidade de gênero corrigida para valor compatível                    | Status de inconsistência **removido**               |

#### Sincronização do benefício "Transcidadania"

| Situação                                                            | Ação automática                          |
| ------------------------------------------------------------------- | ---------------------------------------- |
| Pessoa ativa no programa mas benefício não está no cadastro         | Benefício **adicionado** automaticamente |
| Pessoa não ativa (ou não cadastrada) mas benefício está no cadastro | Benefício **removido** automaticamente   |

### Resumo das sincronizações

<table><thead><tr><th width="179">Evento</th><th width="186.666748046875">O que sincroniza</th><th>Direção</th></tr></thead><tbody><tr><td>Registrar frequência (nova)</td><td>Status, escola, desligamento</td><td>Frequência → Cadastro Transcidadania</td></tr><tr><td>Salvar cadastro Transcidadania</td><td>Escolaridade</td><td>Transcidadania → Pessoa</td></tr><tr><td>Salvar cadastro Transcidadania</td><td>Benefício "Transcidadania"</td><td>Transcidadania → Pessoa (benefícios)</td></tr><tr><td>Salvar cadastro Pessoa</td><td>Consistência de gênero</td><td>Pessoa → Transcidadania (flag inconsistente)</td></tr><tr><td>Salvar cadastro Pessoa</td><td>Benefício "Transcidadania"</td><td>Pessoa ↔ Transcidadania (adiciona/remove)</td></tr></tbody></table>

***

## Cálculo de Frequência e Pagamento

O sistema calcula automaticamente a frequência total mensal, a faixa de desconto e o valor de pagamento com base nos percentuais informados pelo técnico.

### Fórmula de cálculo da frequência total

#### A partir de 2025

```
Frequência Total = (Frequência Escolar × 60%) + (Frequência Atividades Complementares × 40%)
```

<table><thead><tr><th width="402">Componente</th><th>Peso</th></tr></thead><tbody><tr><td>Frequência Escolar</td><td>60%</td></tr><tr><td>Frequência em Atividades Complementares</td><td>40%</td></tr></tbody></table>

#### Antes de 2025

```
Frequência Total = (Frequência Escolar × 70%) + (Frequência Atividades Práticas × 15%) + (Frequência Atividades Teóricas × 15%)
```

| Componente                        | Peso |
| --------------------------------- | ---- |
| Frequência Escolar                | 70%  |
| Frequência em Atividades Práticas | 15%  |
| Frequência em Atividades Teóricas | 15%  |

### Faixas de desconto

#### A partir de 2026

| Frequência Total | Desconto                  | Label          |
| ---------------- | ------------------------- | -------------- |
| Acima de 89%     | Nenhum                    | SEM DESCONTO   |
| 80% a 89%        | 1/30 do valor (R$ 56,74)  | Descontar 1/30 |
| 70% a 79%        | 2/30 do valor (R$ 113,47) | Descontar 2/30 |
| 60% a 69%        | 3/30 do valor (R$ 170,21) | Descontar 3/30 |
| 50% a 59%        | 4/30 do valor (R$ 226,94) | Descontar 4/30 |
| Abaixo de 50%    | 100% (não pagar)          | NÃO PAGAR      |

#### Antes de 2026

| Frequência Total | Desconto | Label                         |
| ---------------- | -------- | ----------------------------- |
| Acima de 89%     | 0%       | SEM DESCONTO                  |
| 80% a 89%        | 5%       | 5%                            |
| 70% a 79%        | 10%      | 10%                           |
| 60% a 69%        | 15%      | 15%                           |
| 50% a 59%        | 20%      | 20%                           |
| 40% a 49%        | 25%      | 25%                           |
| 25% a 39%        | 100%     | NÃO PAGAR                     |
| Abaixo de 25%    | 100%     | POSSIBILIDADE DE DESLIGAMENTO |

### Cálculo do valor de pagamento

```
Valor de Pagamento = Valor Anual do Benefício × (1 - Desconto)
```

O valor final é arredondado para baixo (truncado) em 2 casas decimais.

#### Exemplo prático (2026)

* Valor anual do benefício configurado: R$ 1.702,13
* Frequência escolar: 85%
* Frequência atividades complementares: 70%
* Frequência total = (85 × 0,60) + (70 × 0,40) = 51 + 28 = **79%**
* Faixa: 70% a 79% → Desconto de 2/30
* Valor de pagamento = R$ 1.702,13 × (1 - 2/30) = R$ 1.702,13 × 0,9333 = **R$ 1.588,65**

### Valor anual do benefício

O valor base do benefício é configurado por ano pelo administrador na tela de Configurações (seção Pagamentos > Histórico de Valores Anuais). Ao alterar o valor de um ano, todas as frequências daquele ano são recalculadas automaticamente com o novo valor base.

### Observações

* O campo "Pagamento" é apresentado como **referência** no formulário de frequência. O valor final do pagamento, realizado pela SMDET, pode ser diferente.
* O cálculo é executado em tempo real conforme o técnico preenche os percentuais de frequência.
* Frequências com desconto "NÃO PAGAR" ou "POSSIBILIDADE DE DESLIGAMENTO" são contabilizadas para a regra de inconsistência por excesso de faltas (3 meses em 12).
