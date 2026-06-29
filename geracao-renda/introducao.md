# Introdução

## Introdução ao Programa de Geração de Renda

O módulo **Programa de Geração de Renda** no SIAD é dedicado à gestão do programa de inclusão produtiva da SMDHC, que oferece oportunidades de qualificação profissional e geração de renda para pessoas em situação de vulnerabilidade social atendidas pela secretaria.

O módulo permite cadastrar as pessoas participantes, acompanhar seu status no programa (ativo ou desligado) e documentar o planejamento individual de cada pessoa por meio do PIA (Plano Individual de Atendimento), composto por formulários dinâmicos configuráveis.

***

### Hierarquia do módulo

```
Programa de Geração de Renda
├── Cadastro (vínculo da pessoa ao programa)
│   ├── Pessoa vinculada (obrigatório)
│   ├── Equipamento de vínculo
│   ├── Status (Ativo / Inativo)
│   ├── Data de inserção
│   ├── Data e motivo de desligamento (se inativo)
│   └── Observações
│
└── PIA — Plano Individual de Atendimento
    ├── Múltiplos formulários configuráveis
    ├── Registro por pessoa cadastrada
    ├── Histórico de alterações campo-a-campo
    └── Impressão individual ou em lote
```

***

### Status no programa

O módulo trabalha com dois status:

<table><thead><tr><th width="165.3333740234375">Status</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Ativo</strong></td><td>Pessoa participando do programa.</td></tr><tr><td><strong>Inativo</strong></td><td>Pessoa desligada do programa. Requer data e motivo de desligamento.</td></tr></tbody></table>

#### Motivos de desligamento disponíveis

* Direcionamento ao mercado de trabalho formal
* Direcionamento a cooperativa
* Direcionamento ao POT
* Desistência
* Excesso de faltas
* Infração ao Termo de Convivência
* Saída para o mercado de trabalho informal
* Saída por motivos de saúde
* Saída por tempo de permanência

***

### O que o módulo oferece

#### Cadastro no programa

Formulário de inserção que vincula a pessoa ao programa com equipamento, status, data de inserção e observações. Cada pessoa pode ter apenas um cadastro ativo no programa.

#### PIA — Plano Individual de Atendimento

Conjunto de formulários dinâmicos que documentam o planejamento e a evolução de cada participante. Semelhante ao PIA do Transcidadania, utiliza a mesma infraestrutura de formulários do SIAD (atributos, seções, versões) com histórico detalhado de alterações campo-a-campo.

***

### Diferenças em relação a outros módulos

| Aspecto                             | Geração de Renda                 | Transcidadania                              | SIAD Benefícios                             |
| ----------------------------------- | -------------------------------- | ------------------------------------------- | ------------------------------------------- |
| **Status**                          | Ativo / Inativo                  | Ativo / Inativo / Suspenso / Fila de Espera | Dinâmicos (configuráveis por benefício)     |
| **Acompanhamento mensal**           | Não possui                       | Frequência mensal com cálculo de pagamento  | Periodicidade configurável com formulário   |
| **PIA**                             | Sim (formulários dinâmicos)      | Sim (formulários dinâmicos)                 | Não possui                                  |
| **Controle de acesso**              | Módulo habilitado no equipamento | Módulo habilitado + permissões específicas  | Permissões dinâmicas por benefício          |
| **Cálculos financeiros**            | Não possui                       | Desconto e valor de pagamento automáticos   | Não possui                                  |
| **Regras de inconsistência**        | Não possui                       | 4 regras automáticas                        | Não possui                                  |
| **Elegibilidade**                   | Sem restrição                    | Apenas pessoas trans                        | Sem restrição                               |
| **Formulário de cadastro dinâmico** | Não (campos fixos)               | Não (campos fixos)                          | Sim (formulário configurável por benefício) |

***

### Integração com o cadastro de pessoas

O módulo é integrado ao cadastro de pessoas do SIAD:

* Toda pessoa cadastrada no programa deve existir previamente como pessoa no SIAD
* A aba **"Programa de Geração de Renda"** aparece na sidebar do perfil da pessoa (quando o módulo está habilitado no equipamento do usuário)
* A sidebar exibe um badge com o status atual no programa (ATIVO/INATIVO)
* O cadastro pode ser feito tanto pela listagem centralizada quanto diretamente pela aba no perfil da pessoa
* Na listagem, ao clicar em um cadastro, o sistema redireciona para a página da pessoa no módulo

***

### Pré-requisitos para acesso

Para que o módulo fique visível para um usuário, o **equipamento** ao qual ele está vinculado deve ter o módulo **"Programa de Geração de Renda"** habilitado em suas configurações.

Quando essa condição é atendida, o usuário passa a visualizar:

* O menu **Programa de Geração de Renda > Cadastro** no módulo de Atendimento
* A aba **"Programa de Geração de Renda"** no perfil das pessoas (sidebar)

Para operações administrativas (ver cadastros de todos os equipamentos, gerenciar configurações), o usuário precisa da permissão `GERACAO_RENDA_ADMINISTRAR`.

***

### Navegação no sistema

| Menu                                             | Funcionalidade                                                                    |
| ------------------------------------------------ | --------------------------------------------------------------------------------- |
| **Programa de Geração de Renda > Cadastro**      | Listagem centralizada de todas as pessoas cadastradas no programa                 |
| **Programa de Geração de Renda > Configurações** | Configurações administrativas (formulários PIA, callout) — apenas administradores |
| **Pessoa > aba Programa de Geração de Renda**    | Visão individual da pessoa no programa (cadastro + PIA)                           |
