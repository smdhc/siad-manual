# Criar uma seção

As seções organizam os campos do formulário em blocos temáticos. Cada seção aparecerá como um agrupamento visual para o usuário que preenche o formulário. Além disso, é possível condicionar a exibição de uma seção a partir de outros campos do formulário.

## Como acessar

1. Na listagem de versões, clique no número exibido na coluna **# Seções Cadastradas**, ou
2. Clique na ação **Seções** da versão desejada

\<imagem da listagem de versões com destaque na coluna de seções e no botão "Seções">

#### Campos do cadastro

| Campo      | Obrigatório | Descrição                                                                                              |
| ---------- | ----------- | ------------------------------------------------------------------------------------------------------ |
| Título     | Sim         | Nome da seção que será exibido ao usuário (ex: "Dados Pessoais", "Informações do Projeto").            |
| Descrição  | Não         | Texto auxiliar exibido abaixo do título da seção. Útil para orientações de preenchimento.              |
| Ordem      | Sim         | Número que define a posição da seção no formulário. Seções com menor valor aparecem primeiro.          |
| Colunas    | Sim         | Número de colunas do grid da seção (1 a 12). Define quantos campos podem ficar lado a lado. Padrão: 1. |
| Colapsável | Não         | Quando habilitado, a seção pode ser recolhida/expandida pelo usuário. Padrão: ativado.                 |

\<imagem do modal de criação de seção com os campos preenchidos>

#### Configurações avançadas da seção

**Dependência de campo pai (Seção condicional)**

Uma seção pode ser configurada para aparecer somente quando determinada opção for selecionada em um campo de outra seção.

| Campo      | Descrição                                                                                   |
| ---------- | ------------------------------------------------------------------------------------------- |
| Chave Pai  | O atributo do qual esta seção depende. Somente campos do tipo Lista ou Radio são elegíveis. |
| Opções Pai | Quais valores do campo pai farão esta seção ser exibida.                                    |

**Exemplo:** Uma seção "Dados do Veículo" pode depender de um campo "Possui veículo?" com a opção "Sim" selecionada.

\<imagem do modal de seção com campos de dependência pai preenchidos>

**Pontuação**

Seções podem ter um sistema de pontuação configurado, útil para formulários de avaliação ou processos seletivos.

| Campo                      | Descrição                                                                      |
| -------------------------- | ------------------------------------------------------------------------------ |
| Habilitar Pontuação        | Ativa o cálculo de pontuação para a seção.                                     |
| Exibir pontuação no rodapé | Mostra o subtotal de pontos ao final da seção.                                 |
| Tipo de Agregação          | Como os pontos dos campos serão consolidados: **Soma** ou **Média Ponderada**. |
| Peso da Seção              | Peso relativo da seção no cálculo geral (padrão: 1).                           |

\<imagem do modal de seção com configurações de pontuação habilitadas>
