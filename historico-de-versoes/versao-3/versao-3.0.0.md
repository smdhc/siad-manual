---
description: 'Data de lançamento: 27/02/2025'
---

# Versão 3.0.0

A **versão 3.0.0** do SIAD traz um grande conjunto de melhorias, bem como as novas funcionalidades para gestão do **Programa Transcidadania** e **Monitoramento de Projetos** da SMDHC.

Confira abaixo todos os detalhes dessa atualização.

## Novas funcionalidades

### Transcidadania

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>Tela de cadastro das pessoas beneficiárias do Programa Transcidadania</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1).png" alt=""><figcaption><p>Transcidadania no Cadastro de Pessoas</p></figcaption></figure>

Foi implementada uma nova tela de cadastro para as pessoas beneficiárioas do Programa Transcidadania, que facilitará o controle e acompanhamento por parte dos <mark style="color:purple;">Centros de Referência LGBTI+</mark> e da própria <mark style="color:purple;">Coordenação</mark>.

Nesse primeiro momento, está disponível apenas o cadastro da pessoa beneficiária e a inclusão na fila de espera, que ficará disponível dentro do <mark style="background-color:blue;">Cadastro de Pessoas</mark> ou através do novo menu lateral <mark style="background-color:blue;">Transcidadania > Cadastro</mark>.

Está previsto para a próxima versão o acompanhamento mensal, que irá conter os dados da frequência escolar e outras informações.

{% hint style="warning" %}
O módulo do Transcidadania está disponível somente para os Centros de Referência LGBTI+ e será liberado gradativamente após capacitação das equipes.
{% endhint %}

### Monitoramento de Projetos

<figure><img src="../../.gitbook/assets/image (4) (1) (1) (1).png" alt=""><figcaption><p>Novo módulo de Planejamento</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (3) (1) (1) (1).png" alt=""><figcaption><p>Tela de cadastro de projetos</p></figcaption></figure>

Está disponível um novo módulo de Planejamento do SIAD, que será de uso exclusivo das Coordenadorias e Coordenações da SMDHC.

Nesse primeiro momento, foi disponibilizada uma ferramenta para gestão dos projetos das áreas, que facilitará o monitoramento de projetos prioritários.

## Melhorias

### Encaminhamento para Gerontólogo

Foi adicionada a nova área de encaminhamento interna "Gerontólogo" no registro de <mark style="background-color:blue;">Encaminhamentos</mark> do <mark style="background-color:purple;">Cadastro de Pessoas</mark>. Essa opção ficará disponível somente para equipamentos da temática Pessoa Idosa.

### Novos tipos de atributos do formulário de Atendimento

Foram disponibilizados novos tipos de perguntas para o <mark style="background-color:orange;">formulario de atendimento</mark>, como o "Radio", que permite fazer uma pergunta de múltipla escolha, e Listas Dinâmicas, que permitirão criar formulários mais personalizados de acordo com as respostas.

### Preenchimento automático do equipamento na tela de login

A <mark style="background-color:orange;">tela de login</mark> passa a preencher automaticamente o campo de equipamento caso o usuário possua vínculo somente em um equipamento.

### Equipamentos - Rede de Atendimento SMDHC

Foi adicionada uma nova opção ao <mark style="background-color:purple;">Cadastro de Equipamentos</mark> que permitirá informar se um equipamento faz parte da Rede de Atendimentos SMDHC. Além disso, também será possível filtrar por esses equipamentos no <mark style="background-color:blue;">Relatório de Equipamentos</mark>.

### Benefícios - Outros e Observações

Inclusão da opção "Outros" na lista de benefícios do Cadastro de Pessoas e Composição Familiar. Além disso, foi adicionado um novo campo de observações do benefício.

### Bloqueio de edição do CPF

A partir dessa versão, não será mais possível alterar o CPF de um cadastro depois de criado. Essa medida visa evitar que os cadastros sejam reaproveitados para outras pessoas.

### Remoção da coluna Pessoas no Atendimento

Será removida a coluna "Pessoas" da tela principal de atendimentos, por causar confusão com relação ao seu conceito original, que seria contabilizar participantes em atividades coletivas.

### Novo ícone do sistema

Adicionado novo ícone do sistema que passa a ser exibido na aba do navegador.

## Ajustes e Correções

### Erro de Atendimento com Profissional excluído

Corrigido erro no registro de atendimento que não exibida corretamente o profissional do atendimento caso o mesmo tivesse sido excluído do equipamento.

### Filtro de data de atendimento

Corrigido o filtro de data da tela de atendimentos, que estava considerando a data do registro ao invés da data informada para o atendimento.

### Criação de acesso para usuário inativo

Corrigido erro que impossibilitava vincular um usuário a um novo equipamento caso o mesmo tivesse sido excluído em outro equipamento anteriormente.

### Indicador de usuários ativos

Corrigido o indicador de usuários ativos da tela inicial para considerar usuários únicos.

### Exclusão de atendimento internos

Corrigida brecha que permitia alterar/excluir atendimentos históricos importados para o sistema, caso o usuário não seja Administrador.
