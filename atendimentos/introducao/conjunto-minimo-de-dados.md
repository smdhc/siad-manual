# Conjunto Mínimo de Dados

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Para que um registro seja considerado um atendimento, é necessário que responda <mark style="color:red;">**obrigatoriamente**</mark> às seguintes perguntas:

| Pergunta    | Descrição                                                               |
| ----------- | ----------------------------------------------------------------------- |
| **O quê?**  | Qual fato ocorreu, tipo de atendimento, tipo de atividade, serviço etc. |
| **Onde?**   | Em qual equipamento, local, modalidade…                                 |
| **Quando?** | Data/hora do acontecimento                                              |
| **Quanto?** | Quantas pessoas foram atendidas, quantas atividades, quantas ações…     |

As respostas a essas perguntas compõem o **conjunto mínimo de dados** que todo registro de atendimento deve conter, <mark style="color:purple;">independentemente de sua natureza</mark>.

<mark style="background-color:orange;">Exemplo</mark> de um registro de atendimento com conjunto mínimo de dados:

| Pergunta    | Equivalência        | Resposta             |
| ----------- | ------------------- | -------------------- |
| **O quê?**  | Tipo de Atendimento | Orientações diversas |
| **Onde?**   | Equipamento         | NDH Central          |
| **Quando?** | Data do Atendimento | 23/12/2024           |
| **Quanto?** | Quantidade          | 1                    |

{% hint style="warning" %}
A definição de um conjunto mínimo de dados não impede a coleta de informações adicionais; ela apenas estabelece a estrutura essencial necessária para que um registro seja considerado um atendimento.
{% endhint %}

### Tipo de Atendimento

Como mencionado anteriormente, um dos atributos fundamentais que compõem o registro de atendimento é o **Tipo de Atendimento**, que <mark style="color:purple;">caracteriza</mark> o atendimento e define quais outras informações serão coletadas em cada registro.

São exemplos de tipo de atendimento:

* Atendimento Inicial
* Atendimento Técnico Psicossocial
* Oficina
* Uso de Lavanderia
* Entre outros.

Cada tipo de atendimento poderá ter um formulário distinto, mas todos compartilharão o mesmo conjunto mínimo de dados.

### Dados históricos

<figure><img src="../../.gitbook/assets/image (7) (1) (1).png" alt=""><figcaption></figcaption></figure>

Uma das grandes vantagens desse modelo é a possibilidade de <mark style="background-color:green;">aproveitar e importar dados históricos</mark>.

Até mesmo dados antigos, desestruturados e fragmentados poderão ser convertidos e estruturados no novo formato, desde que contenham o conjunto mínimo de dados.

{% hint style="info" %}
A importação dos dados históricos será realizada de forma gradual, à medida que a funcionalidade for sendo expandida para os equipamentos da nossa rede.
{% endhint %}
