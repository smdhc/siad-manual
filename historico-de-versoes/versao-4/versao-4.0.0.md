---
description: 'Data de lançamento: 04/04/2025'
---

# Versão 4.0.0

A **versão 4.0.0** do SIAD é uma versão que traz a <mark style="background-color:yellow;">nova funcionalidade</mark> de **Acompanhamento do Transcidadania**, <mark style="background-color:green;">revisão</mark> das regras de **sigilo** do Cadastro de Pessoas, além de <mark style="background-color:blue;">ajustes</mark> diversos no sistema em geral.

Confira abaixo todos os detalhes dessa atualização.

## Novas funcionalidades

### Transcidadania - Acompanhamento Mensal

<figure><img src="../../.gitbook/assets/image (169).png" alt=""><figcaption><p>Nova tela de acompanhamento do Transcidadania</p></figcaption></figure>

Foi implementada uma nova tela de acompanhamento das pessoas beneficiárioas do Programa Transcidadania, que permitirá o registro da <mark style="color:purple;">Frequência Escolar</mark> mensal.

Além disso, foi implementada também uma tela de configurações específica para o Transcidadania, que no momento, permite configurar o prazo de preenchimento do acompanhamento mensal.

{% hint style="warning" %}
O módulo do Transcidadania está disponível somente para os Centros de Referência LGBTI+ e será liberado gradativamente após capacitação das equipes.
{% endhint %}

## Melhorias

### Cadastro de Pessoas - Revisão de Sigilo

<figure><img src="../../.gitbook/assets/image (170).png" alt=""><figcaption></figcaption></figure>

Informamos que as regras de exibição do sigilo de cadastro foram modificadas para atender à expansão do sistema à **rede de atendimento às mulheres**.

Essa atualização tem como objetivo aprimorar a <mark style="color:red;">segurança e a privacidade</mark> das usuárias, garantindo conformidade com as diretrizes de proteção de dados e boas práticas no atendimento especializado. Além disso, a nova configuração permitirá um acesso mais amplo às informações por parte dos profissionais devidamente autorizados, assegurando que o compartilhamento de dados ocorra de forma controlada, com registros detalhados para fins de auditoria e rastreabilidade.

Confira abaixo as principais alterações:

* Cadastros sigilosos passam a ser <mark style="background-color:green;">acessíveis em toda a rede</mark> de atendimento, com a ressalva de que os dados de endereço e contato somente ficarão disponíveis mediante <mark style="background-color:orange;">justificativa</mark>.
* Maior <mark style="color:blue;">controle e auditabilidade</mark> dos acessos realizados em cadastros sigilosos.
* Todos os submenus do Cadastro da Pessoa passam a exibir um <mark style="color:orange;">alerta em caso de sigilo</mark>.
* **Anexos antigos** passam a ser visíveis somente para <mark style="color:orange;">equipamentos de mesma temática</mark>, além de não exibir mais as informações do equipamento que inseriu.
* Implementado novo **controle de visibilidade** para novos anexos, permitindo selecionar quem poderá ver ([versão 4.0.1](versao-4.0.1.md)).
* Restrição no acesso aos **prontuários** cadastrados, de forma a não exibir prontuários associados em equipamentos sigilosos ou ouvidoria.
* Restrição no **histórico de atendimentos** da pessoa, de forma a não exibir atendimentos realizados em equipamentos sigilosos ou ouvidoria.
* Revisão geral das regras de acesso e consulta aos **encaminhamentos**:
  * Se a origem ou destino forem equipamentos sigilosos, somente os equipamentos envolvidos terão acesso;
  * Se a origem ou destino forem equipamentos da ouvidoria, somente equipamentos da ouvidoria terão acesso (além do outro equipamento envolvido).
  * Demais casos são acessíveis para toda a rede (somente dados básicos, os detalhes são restritos aos equipamentos de mesma temática).

### Cadastro de Pessoas - Nome Retificado

Foi adicionada uma nova pergunta <mark style="background-color:purple;">"Possui nome retificado?"</mark> ao **Cadastro de Pessoas** (aba Dados Sociodemográficos), que ficará visível e de preenchimento obrigatório quando a Identidade de Gênero selecionada for:

* Homem Trans;
* Mulher Transexual;
* Travesti;
* Não Binário.

### Projetos - Dados complementares e outras melhorias

<figure><img src="../../.gitbook/assets/image (171).png" alt=""><figcaption><p>Seção "Dados Complementares" no Cadastro de Projetos</p></figcaption></figure>

Adicionada nova etapa obrigatória no Cadastro de Projetos, contendo dados complementares que auxiliarão na etapa de priorização.

Também foi adicionado o campo para Motivo do Travamento, caso o status do projeto seja Travado.

Além disso, alguns títulos de telas e colunas na listagem de projetos foram revisados e atualizados.

{% hint style="info" %}
O Cadastro de Projetos é uma funcionalidade disponível somente para as áreas internas da SMDHC.
{% endhint %}

### Atendimentos - Campo "Menor desacompanhado" dinâmico

O atributo de atendimento "Menor desacompanhado" (exclusivo de equipamentos de imigrantes) passa a ser dinâmico, permitindo que outros campos fiquem visíveis dependendo da opção selecionada.

### Atendimentos - Vínculo de atividade coletiva no histórico da pessoa

O registro de atendimento de atividades coletivas com múltiplas pessoas informadas no formulário de atendimento passa a ser exibido no histórico de atendimentos dessas pessoas.

### Composição Familiar - Dependente e Responsável Legal

<figure><img src="../../.gitbook/assets/image (173).png" alt=""><figcaption><p>Novas opções de Ligações Familiares</p></figcaption></figure>

Foram adicionadas as opções <mark style="background-color:blue;">"Dependente"</mark> e <mark style="background-color:blue;">"Responsável Legal"</mark> no campo "**Ligação Familiar**", da janela de cadastro da Composição Familiar.

Com isso, a antiga pergunta "<mark style="background-color:purple;">É responsável legal?</mark>", que era exibida quando a pessoa do cadastro era menor de 18 anos, foi <mark style="color:red;">removida</mark>, dando lugar a essa opção.

Todos os membros familiares que estavam com essa opção habilitada foram atualizados automaticamente com a opção "Responsável Legal" na ligação familiar.

### Transcidadania - Ano letivo de evasão escolar

<figure><img src="../../.gitbook/assets/image (172).png" alt=""><figcaption></figcaption></figure>

O campo "Ano letivo de evasão escolar" no Cadastro do Transcidadania passa a ser uma lista fechada, com valores pré-definidos.

### Painel de controle

Foi aplicado o separador de milhar nos indicadores de cadastro e atendimento da página inicial do SIAD.

## Ajustes

### Cadastro de Pessoas - Atualização de benefícios

Os benefícios abaixo tiveram seus nomes corrigidos:

* Auxílio-Acidente
* Auxílio-Doença
* Auxílio-Reclusão

A mudança foi aplicada no Cadastro de Pessoas (aba Dados Socioeconômicos) e no cadastro da Composição Familiar.

### Cadastro de Pessoas - Limpeza de nomes

Foi aplicada uma limpeza nos campos abaixo, removendo espaços em branco em excesso:

Cadastro de pessoas:

* Nome civil
* Nome social
* Nome da mãe
* Nome do pai

Composição familiar:

* Nome

### Atendimentos - Correção de bug em campos dinâmicos

Foi corrigido um bug que mantinha campos do formulário de atendimento visíveis mesmo após suas condições de visibilidade terem sido alterados.
