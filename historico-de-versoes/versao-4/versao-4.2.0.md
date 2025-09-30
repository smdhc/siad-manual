---
description: 'Data de lançamento: 16/05/2025'
---

# Versão 4.2.0

A **versão 4.2.0** do SIAD é uma versão que traz <mark style="background-color:yellow;">novas funcionalidades</mark> como o **RCC, Programa de Geração de Renda e preenchimento automático de Distrito**, além de <mark style="background-color:blue;">ajustes</mark> e <mark style="background-color:green;">melhorias</mark> diversas no sistema em geral.

Confira abaixo todos os detalhes dessa atualização.

## Novas funcionalidades

### Cidade Solidária - Prestação de Contas (Versão preliminar)

Foi disponibilizado um novo formulário para prestação de contas do Programa Cidade Solidária, restrita à equipe da SESANA.

Trata-se de uma versão preliminar, que ainda passará por ajustes e melhorias.

### Programa de Geração de Renda

<figure><img src="../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

Foi adicionada uma nova seção "<mark style="background-color:purple;">Programa de Geração de Renda</mark>", no Cadastro de Pessoas, de uso exclusivo dos equipamentos Recifran e Reviravolta, para fins de registro de informações dos participantes cadastrados no programa.

### RCC (Versão preliminar)

Foi disponibilizada uma nova funcionalidade, restrita à equipe da SESANA, para a gestão da fila de restaurantes credenciados no programa Rede Cozinha Cidadã.

Trata-se de uma versão preliminar, que ainda passará por ajustes e melhorias.

## Melhorias

### Atendimentos - Número de Protocolo

<figure><img src="../../.gitbook/assets/image (182).png" alt=""><figcaption></figcaption></figure>

Foi adicionado o número de protocolo à tela de visualização do atendimento. Esse número servirá como identificador único do registro e poderá ser utilizado na busca por meio da lupa na tela de listagem de atendimentos.

### Atendimentos - Filtro por Tipo de Atendimento

O filtro "Tipo de Atendimento" passa a exibir somente os tipos configurados para o equipamento logado.

### Cadastro de Pessoas - Preenchimento de Distrito automático

<figure><img src="../../.gitbook/assets/image (181).png" alt=""><figcaption></figcaption></figure>

A partir desta versão, a pesquisa de CEPs do município de São Paulo preencherá automaticamente o campo de <mark style="background-color:blue;">Distrito</mark>, nas seguintes funcionalidades:

* Cadastro de Pessoas
* Cadastro de Equipamentos
* Cadastro de Organizações

Além disso, os campos foram reorganizados para seguir uma ordem mais coerente com o fluxo de preenchimento.

{% hint style="warning" %}
A pesquisa de CEPs depende da disponibilidade do serviço externo "LocalizaSampa". Dessa forma, o distrito não será preenchido automaticamente caso este serviço esteja fora do ar ou caso não haja uma correspondência direta com o CEP informado. Os CEPs consultados com sucesso serão armazenados no sistema para futuras consultas.
{% endhint %}

{% hint style="warning" %}
Assim que a nova versão for disponibilizada no ambiente de Produção, será executado um script que irá atualizar os dados de endereço de todos os CEPs cadastrados na base de pessoas e equipamentos.
{% endhint %}

### Infraestrutura - Atualização da versão do PHP

A versão do PHP — linguagem de programação utilizada no desenvolvimento do sistema — foi atualizada para a 8.3, trazendo melhorias de desempenho e maior compatibilidade com determinadas bibliotecas.

### Transcidadania - Mês padrão na tela de acompanhamento

A tela de acompanhamento do Transcidadania foi alterada de forma a exibir as frequências do mês anterior por padrão, ao invés do mês atual.

## Ajustes

### Atendimentos - Erro ao excluir atributo

Foi corrigido um erro que ocorria ao abrir atendimentos contendo atributos previamente excluídos. Além disso, o sistema agora impede a exclusão de atributos que estejam vinculados a um ou mais tipos de atendimento.

### Atendimentos - Exibição de profissionais excluídos

Foi corrigido um erro que impedia a exibição correta do nome de profissionais excluídos na tela de visualização de atendimentos. O problema ocorria apenas em atendimentos cuja lista de profissionais estivesse configurada como um atributo complementar.

### Atendimentos/Encaminhamentos - Listagem com perfil Administrador

As regras de exibição e listagem de atendimentos e encaminhamentos para usuários com perfil de Administrador foram ajustadas, permitindo a visualização de todos os registros sem restrições. Essa alteração visa facilitar a identificação e resolução de casos duplicados, que requerem acesso completo ao histórico do sistema.

### Atendimentos - Remoção de sigilo

Foi corrigida a regra de remoção de sigilo de atendimentos. Além do usuário que originalmente habilitou o sigilo, agora também será permitida a remoção por usuários com a permissão específica ATENDIMENTO\_REMOVER\_SIGILO, que será futuramente atribuída a perfis como Supervisão Técnica ou Coordenador do equipamento.

### Cadastro de Pessoas - Correção de erro em cadastros sem idade

Foi corrigido um erro que ocorria ao acessar cadastros sem data de nascimento ou idade aproximada informadas — cenário presente apenas em registros provenientes de importações.

### Transcidadania - Correção de configuração

A tela de configurações do Transcidadania foi realocada para o módulo Admin, deixando de estar disponível nos demais módulos do sistema. Além disso, o campo de configuração do prazo de preenchimento (em dias) foi aprimorado para aceitar apenas valores numéricos, evitando erros decorrentes de configurações inadequadas.
