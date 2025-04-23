---
description: 'Data de lançamento: 24/04/2025'
---

# Versão 4.1.0

A **versão 4.1.0** do SIAD é uma versão que traz a <mark style="background-color:yellow;">nova funcionalidade</mark> de **Acompanhamento do Transcidadania**, <mark style="background-color:green;">revisão</mark> das regras de **sigilo** do Cadastro de Pessoas, além de <mark style="background-color:blue;">ajustes</mark> diversos no sistema em geral.

Confira abaixo todos os detalhes dessa atualização.

## Novas funcionalidades

### Central de Encaminhamentos

<figure><img src="../../.gitbook/assets/image (179).png" alt=""><figcaption></figcaption></figure>

Implementada nova tela para que os usuários possam facilmente consultar todos os encaminhamentos realizados no equipamento.

Além disso será possível aplicar diversas combinações de filtros, bem como visualizar e editar os encaminhamentos consultados.

Essa funcionalidade ficará disponível através do menu <mark style="background-color:blue;">Cadastros > Encaminhamentos</mark>.

{% hint style="info" %}
Em breve, será implementada uma outra aba nessa tela que permitirá também consultar os **encaminhamentos recebidos** através de outros equipamentos da rede de atendimento da SMDHC.
{% endhint %}

### Painéis dinâmicos

<figure><img src="../../.gitbook/assets/image (175).png" alt=""><figcaption></figcaption></figure>

Foi implementada uma nova funcionalidade para acessar diversos painéis de indicadores do SIAD. Essa funcionalidade permite com que os Administradores do sistema disponibilizem novos painéis de forma totalmente dinâmica e configurável, sem precisar que novas versões do SIAD sejam implantadas.

Através dessa funcionalidade será possível visualizar indicadores diversos de cadastro de pessoas, atendimentos, encaminhamentos, programas etc., podendo ser segmentada pela temática dos equipamentos.

A funcionalidade estará disponível através do menu <mark style="background-color:blue;">Relatórios > Painéis</mark>.

{% hint style="info" %}
A disponibilização de painéis será realizada gradativamente conforme alinhamento a ser realizado com as coordenações temáticas.
{% endhint %}

{% hint style="warning" %}
A funcionalidade anterior "Relatórios" foi renomeada para "Exportações", pois passará a lidar exclusivamente com a exportação de dados no formato de planilhas.
{% endhint %}

### Cadastro de Pessoas - Exclusão de duplicidades

<figure><img src="../../.gitbook/assets/image (176).png" alt=""><figcaption></figcaption></figure>

A partir dessa versão será possível excluir cadastros identificados como duplicados.

Uma vez excluído, o cadastro deixará de ser exibido no sistema, bem como todos os seus registros associados (atendimentos, encaminhamentos etc.).

Caso a exclusão seja realizada de forma equivocada, será possível reativar o cadastro, bem como todos os registros associados.

Antes de excluir o cadastro, também será possível selecionar e transferir os registros associados do cadastro duplicado para o cadastro identificado como principal, permitindo assim o reaproveitamento de dados que foram registrados em ambos os cadastros.

{% hint style="danger" %}
Nesse momento, todos os recursos apresentados acima estarão restritos aos administradores do sistema.
{% endhint %}

{% hint style="warning" %}
Caso identifique algum cadastro duplicado, envie um e-mail para siad@prefeitura.sp.gov.br informando o código SIAD de ambos, para que a nossa equipe possa analisar e remover as duplicidades.
{% endhint %}

## Melhorias

### Atendimentos - Exibição de dados complementares

<figure><img src="../../.gitbook/assets/image (177).png" alt=""><figcaption></figcaption></figure>

Para facilitar a visualização dos atendimentos na listagem do menu "Atendimentos" e no histórico da pessoa, será possível agora configurar a exibição de dados complementares do atendimento ao passar o mouse por cima do Tipo de Atendimento.

Essa configuração será realizada de forma opcional de acordo com cada Tipo de Atendimento e de acordo com alinhamento a ser realizado com cada coordenação temática.

### Atendimentos - Filtro de Menor Desacompanhado

Adicionado novo filtro que permite consultar os atendimentos realizados para menor desacompanhado. Essa função estará disponível somente para equipamentos de imigrantes.

## Ajustes

### Atendimentos - Consulta de atendimentos com múltiplos participantes

Corrigida falha na visualização de atendimentos configurados para permitir múltiplos participantes (como no caso de atividades coletivas), onde ao invés do nome das pessoas, era exibido seus códigos de identificação no sistema.

### Atendimentos - Erro ao editar atendimentos com múltiplos profissionais

Corrigido erro que era exibido ao editar um atendimento registrado com múltiplos profissionais. O erro somente era exibido em situações específicas, em atendimentos registrados com múltiplos profissionais cujo tipo de atendimento havia sido alterado para permitir somente um único profissional.

### Atendimentos - Validação de configurações

Adicionadas validações nos campos quantitativos da tela de configurações dos tipos de atendimentos.

### Cadastro de Pessoas - Códigos SIAD duplicados

Foi ajustado o algoritmo de geração do Código SIAD para evitar que duas pessoas distintas possam receber o mesmo código.
