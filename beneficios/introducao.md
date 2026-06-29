# Introdução

## SIAD Benefícios — Introdução

O **SIAD Benefícios** é o módulo do SIAD voltado à gestão de benefícios e programas sociais ofertados pela SMDHC, como Auxílio Aluguel, Auxílio Ampara, POTs e demais auxílios. Ele permite configurar, operar e acompanhar a concessão de benefícios de forma dinâmica, com formulários personalizáveis e controle granular de acesso.

***

## Para que serve

O módulo centraliza o ciclo de vida completo de um benefício social:

* **Configuração** do benefício pelo gestor (definir formulários, status, equipamentos habilitados, permissões)
* **Cadastro** de beneficiários pelos técnicos (vincular pessoas ao benefício com formulário dinâmico)
* **Acompanhamento** periódico dos beneficiários (registros mensais, bimestrais, trimestrais etc.)
* **Visão gerencial** de pendências (quais beneficiários ainda não tiveram acompanhamento registrado no período)

***

## Diferenças em relação ao SIAD Forms

Embora ambos os módulos utilizem os mesmos formulários dinâmicos (atributos, seções, versões), o SIAD Benefícios possui escopo e comportamento distintos:

| Aspecto                       | SIAD Forms                                                   | SIAD Benefícios                                                              |
| ----------------------------- | ------------------------------------------------------------ | ---------------------------------------------------------------------------- |
| **Propósito**                 | Coleta de dados genérica via fluxos e etapas                 | Gestão de benefícios sociais com vínculo obrigatório a pessoas               |
| **Acesso**                    | Público ou interno (por etapa)                               | Exclusivamente interno (requer login)                                        |
| **Vínculo com Pessoa**        | Opcional (depende do formulário)                             | Obrigatório — todo cadastro é vinculado a uma pessoa do SIAD                 |
| **Estrutura**                 | Fluxo → Versão → Etapas → Protocolo → Respostas              | Benefício → Cadastros (beneficiários) → Acompanhamentos                      |
| **Acompanhamento**            | Etapas intermediárias (livre)                                | Periodicidade configurável com controle de pendências                        |
| **Permissões**                | Por fluxo/etapa (Administrador, Editor, regras por entidade) | Dinâmicas por benefício (geradas automaticamente com \~28 permissões por ID) |
| **Restrição por equipamento** | Não possui nativamente                                       | Integrado — técnico só vê cadastros do seu equipamento                       |

***

## Hierarquia do módulo

```
Benefício (Configuração)
├── Informações Gerais (nome, status, descrição)
├── Formulário de Cadastro (vinculado a uma versão publicada)
├── Status Permitidos (ex: Ativo, Inativo, Em Análise, Desligado)
├── Configuração de Acompanhamento (periodicidade + formulário)
├── Equipamentos habilitados
├── Organizações habilitadas
├── Permissões geradas automaticamente
│
└── Cadastros (Beneficiários)
    ├── Pessoa vinculada (obrigatório)
    ├── Equipamento/Organização de vínculo
    ├── Status (dentre os permitidos)
    ├── Atributos (dados do formulário dinâmico)
    │
    └── Acompanhamentos
        ├── Ano + Referência (período)
        ├── Equipamento/Organização
        └── Atributos (dados do formulário de acompanhamento)
```

***

## Ciclo de vida de um benefício

O benefício possui três status de configuração:

<table><thead><tr><th width="172.6666259765625">Status</th><th>Significado</th></tr></thead><tbody><tr><td><strong>Rascunho</strong></td><td>Em construção. Não aparece para os técnicos.</td></tr><tr><td><strong>Publicado</strong></td><td>Ativo e operacional. Técnicos com permissão podem cadastrar beneficiários.</td></tr><tr><td><strong>Arquivado</strong></td><td>Desativado. Não aceita novos cadastros, mas dados existentes permanecem consultáveis.</td></tr></tbody></table>

> Importante: os status do benefício (Rascunho/Publicado/Arquivado) se referem à **configuração**. Os status dos **cadastros** (Ativo, Inativo, Em Análise etc.) são definidos livremente pelo gestor na criação do benefício.

***

## Perfis de uso

O módulo atende dois públicos principais:

### Gestor / Coordenador

Responsável pela **configuração** do benefício:

* Criar e publicar o benefício
* Definir formulários de cadastro e acompanhamento
* Vincular equipamentos e organizações
* Configurar permissões e atribuí-las a perfis
* Consultar a visão gerencial de pendências de acompanhamento

### Técnico / Operador

Responsável pela **operação** do dia-a-dia:

* Cadastrar pessoas no benefício (vinculando ao seu equipamento)
* Preencher o formulário socioeconômico do beneficiário
* Alterar o status do cadastro conforme evolução do processo
* Registrar acompanhamentos periódicos
* Consultar e editar cadastros existentes

***

## Sistema de permissões dinâmicas

Uma característica central do SIAD Benefícios é que **cada benefício criado gera automaticamente seu próprio conjunto de permissões**. Isso permite controle granular sem necessidade de intervenção técnica no banco de dados.

Ao criar um benefício de ID `5`, por exemplo, o sistema gera permissões como:

* `BENEFICIARIOS_5_ACESSAR` — ver a aba deste benefício na listagem
* `BENEFICIARIOS_5_CADASTRAR` — cadastrar pessoas neste benefício
* `BENEFICIARIOS_5_ACOMPANHAMENTO_CADASTRAR` — registrar acompanhamentos
* `BENEFICIARIOS_5_ACESSAR_GLOBAL` — ver cadastros de todos os equipamentos (supervisão)

Isso significa que um técnico pode ter acesso ao "Auxílio Aluguel" mas não ao "Auxílio Ampara", por exemplo — tudo controlado por perfis.

***

## Integração com o cadastro de pessoas

Todo cadastro de beneficiário é obrigatoriamente vinculado a uma **pessoa** do SIAD. Isso traz os seguintes benefícios:

* O perfil da pessoa consolida todos os benefícios que ela recebe em uma visão unificada
* É possível cadastrar um beneficiário diretamente a partir do perfil da pessoa (atalho com pré-preenchimento)
* Não é permitido cadastrar a mesma pessoa duas vezes no mesmo benefício (validação de duplicidade)
* A sidebar do beneficiário oferece link direto para retornar ao cadastro completo da pessoa

***

## Integração com formulários dinâmicos

O SIAD Benefícios reutiliza a infraestrutura de formulários do SIAD Forms:

* O gestor cria os formulários no módulo de Formulários (seções, atributos, versões)
* Na configuração do benefício, vincula o formulário desejado e sua versão publicada
* Os técnicos preenchem esses formulários ao cadastrar beneficiários ou registrar acompanhamentos
* Todos os tipos de atributo disponíveis no SIAD Forms funcionam aqui (Texto, Lista, CEP, Repeater, Pontuação etc.)

Isso garante flexibilidade total: cada benefício pode ter seu próprio formulário com campos específicos, sem necessidade de alteração no código do sistema.

***

## Pré-requisitos para colocar um benefício no ar

Resumo do que é necessário, do início ao fim:

1. Criar o **formulário de cadastro** no módulo de Formulários e publicar sua versão
2. Criar o **formulário de acompanhamento** (se aplicável) e publicar
3. Criar o **benefício** com todas as configurações
4. Vincular **equipamentos** e/ou **organizações** que poderão operar
5. Atribuir as **permissões** geradas aos perfis de usuário adequados
6. Alterar o status do benefício para **Publicado**

A partir daí, os técnicos com permissão e equipamento vinculado poderão começar a cadastrar beneficiários.
