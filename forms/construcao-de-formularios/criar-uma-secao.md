# Criar uma seção

As seções organizam os campos do formulário em blocos temáticos. Cada seção aparecerá como um agrupamento visual para o usuário que preenche o formulário. Além disso, é possível condicionar a exibição de uma seção a partir de outros campos do formulário.

## Como acessar

1. Na listagem de versões, clique no número exibido na coluna **# Seções Cadastradas**, ou
2. Clique na ação **Seções** da versão desejada

<figure><img src="../../.gitbook/assets/image (77).png" alt=""><figcaption></figcaption></figure>

## Cadastrar nova seção

Para cadastrar uma nova seção do formulário, clique no botão "Nova seção". Será aberta uma janela de configuração conforme abaixo.

<figure><img src="../../.gitbook/assets/image (83).png" alt=""><figcaption></figcaption></figure>

### Campos do cadastro

<table><thead><tr><th width="147.3333740234375">Campo</th><th width="123">Obrigatório</th><th>Descrição</th></tr></thead><tbody><tr><td>Título</td><td>Sim</td><td>Nome da seção que será exibido ao usuário (ex: "Dados Pessoais", "Informações do Projeto").</td></tr><tr><td>Descrição</td><td>Não</td><td>Texto auxiliar exibido abaixo do título da seção. Útil para orientações de preenchimento.</td></tr><tr><td>Ordem</td><td>Sim</td><td>Número que define a posição da seção no formulário. Seções com menor valor aparecem primeiro.</td></tr><tr><td>Colunas</td><td>Sim</td><td>Número de colunas do grid da seção (1 a 12). Define quantos campos podem ficar lado a lado. Padrão: 1.</td></tr><tr><td>Colapsável</td><td>Não</td><td>Quando habilitado, a seção pode ser recolhida/expandida pelo usuário. Padrão: ativado.</td></tr></tbody></table>

### Configurações avançadas da seção

**Dependência de campo pai (Seção condicional)**

Uma seção pode ser configurada para aparecer somente quando determinada opção for selecionada em um campo de outra seção.

<table><thead><tr><th width="174.6666259765625">Campo</th><th>Descrição</th></tr></thead><tbody><tr><td>Chave Pai</td><td>O atributo do qual esta seção depende. Somente campos do tipo Lista ou Radio são elegíveis.</td></tr><tr><td>Opções Pai</td><td>Quais valores do campo pai farão esta seção ser exibida.</td></tr></tbody></table>

**Exemplo:** Uma seção "Dados do Veículo" pode depender de um campo "Possui veículo?" com a opção "Sim" selecionada.

### **Pontuação**

Seções podem ter um sistema de pontuação configurado, útil para formulários de avaliação ou processos seletivos. Para maiores detalhes, consultar tópico dedicado a esse mecanismo.

| Campo                      | Descrição                                                                      |
| -------------------------- | ------------------------------------------------------------------------------ |
| Habilitar Pontuação        | Ativa o cálculo de pontuação para a seção.                                     |
| Exibir pontuação no rodapé | Mostra o subtotal de pontos ao final da seção.                                 |
| Tipo de Agregação          | Como os pontos dos campos serão consolidados: **Soma** ou **Média Ponderada**. |
| Peso da Seção              | Peso relativo da seção no cálculo geral (padrão: 1).                           |

### Seção criada

Após gravar, a seção será exibida na listagem de seções, permitindo publicar o formulário como está ou avançar nas configurações de atributos/perguntas de cada seção.

<figure><img src="../../.gitbook/assets/image (88).png" alt=""><figcaption></figcaption></figure>

O próximo passo é configurar as perguntas/atributos que irão compor o formulário.
