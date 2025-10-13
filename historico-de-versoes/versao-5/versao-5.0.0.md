---
description: 'Data de lançamento: 30/09/2025'
---

# Versão 5.0.0

A **versão 5.0.0** do SIAD é uma versão que traz a <mark style="background-color:yellow;">nova funcionalidade</mark> do **Programa Cidade Solidária e a integração com CadÚnico**, além de <mark style="background-color:blue;">melhorias e ajustes</mark> diversos no sistema em geral.

Confira abaixo todos os detalhes dessa atualização.

## Novas funcionalidades

### Programa Cidade Solidária

<figure><img src="../../.gitbook/assets/image (192).png" alt=""><figcaption></figcaption></figure>

Foi disponibilizado um novo conjunto de funcionalidades para aprimorar a gestão do novo Programa Cidade Solidária, permitindo também que as entidades se autentiquem e acompanhem o cadastro de suas remessas e beneficiários.

### Integração com CadÚnico

A partir dessa versão, o SIAD passará a contar com a base do CadÚnico, fornecida mensalmente pela SMADS (Secretaria Municipal de Assistência e Desenvolvimento Social).

Nesse primeiro momento, a base será primordialmente utilizada no cadastro de famílias do Programa Cidade Solidária.

Além disso, conforme imagem abaixo, a ficha de cadastro da pessoa já passará a exibir a informação se um cadastro do SIAD está na base do CadÚnico e sua respectiva data da última atualização.

<figure><img src="../../.gitbook/assets/image (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
A base do CadÚnico é atualizada mensalmente e depende da disponibilização periódica por parte da SMADS, podendo assim não exibir a informação de pessoas que foram cadastradas recentemente. Para saber a data da atualização da base, basta passar o mouse por cima do campo "Cadastrada(o) no CadÚnico?".
{% endhint %}

{% hint style="info" %}
Nas próximas versões, a base do CadÚnico poderá ser utilizada para facilitar o processo de cadastro de pessoas, programas e benfícios.
{% endhint %}

## Melhorias

### Atendimentos - Colunas de protocolo e pessoas

<figure><img src="../../.gitbook/assets/image (2) (1) (1).png" alt=""><figcaption></figcaption></figure>

Na funcionalidade de Atendimentos, a coluna "Pessoas" foi reinserida na tabela, acrescida da coluna "Protocolo", que pode ser habilitada através do ícone ao lado do filtro.

As opções de atendimento (Visualizar, Alterar etc.) foram agrupadas para melhorar a disposição das informações na tela.

{% hint style="info" %}
Foi adicionado o seguinte texto ao campo "Pessoas", presente em alguns tipos de atendimento (ex: atividades coletivas):\
&#xNAN;_<mark style="color:$warning;">"Total de pessoas participantes da atividade, independentemente de estarem cadastradas ou não no equipamento. O número informado deve corresponder ao da lista de presença anexada."</mark>_
{% endhint %}

### Atendimentos - Nome dos profissionais

O nome do(a)(s) profissional(is) responsável(is) pelo atendimento, exibido no histórico da pessoa, passará a mostrar apenas a ocupação quando o equipamento logado for de temática diferente daquela em que o atendimento foi realizado.

Essa medida tem como objetivo garantir o sigilo das informações.

{% hint style="info" %}
Caso o profissional não possua a ocupação cadastrada, será exibido "Desconhecido".
{% endhint %}

### Atendimentos - Ocupações

A partir dessa versão será possível configurar, para cada Tipo de Atendimento, as ocupações que poderão ver/registrar o respectivo atendimento.

Essa melhoria representa um avanço significativo com relação à segurança da informação.

{% hint style="info" %}
Essa configuração ocorrerá conforme o cadastro dos profissionais forem atualizados no sistema e de acordo com as regra definidas com cada coordenação temática.
{% endhint %}

### Cadastro de Organizações - Ficha de Cadastro

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1).png" alt=""><figcaption><p>Nova ficha de cadastro da organização</p></figcaption></figure>

O Cadastro de Organizações foi repaginado de forma a seguir o mesmo padrão do Cadastro de Pessoas, o que permitirá visualizar de uma forma mais fácil os seus relacionamentos com equipamentos, programas entre outros.

Além disso, através dessa nova tela, também será possível gerar credenciais de acesso para que as próprias organizações possam acessar o sistema.

{% hint style="info" %}
Nesse primeiro momento, as credenciais de acesso funcionam somente para o Programa Cidade Solidária.
{% endhint %}

### Cadastro de Pessoas - País de Nascimento obrigatório

A partir dessa versão, o campo "País de Nascimento" passará a ser obrigatório ao cadastrar uma nova pessoa no sistema.

Os principais fundamentos para essa mudança são:

* identificar o acesso da população imigrante nos equipamentos da Rede de Direitos Humanos;
*  dar maior visibilidade, por meio do SIAD, à atuação transversal como princípio da Rede, conforme a Portaria 015/SMDHC/2021, em especial o art. 6º;
*  permitir o adequado preenchimento e diminuir a subnotificação de informações concernentes à população imigrante, considerando as complexidades que esta população já enfrenta para ser identificada nos diferentes sistemas de registro disponíveis na rede pública; e,
*  fornecer informações de forma completa e precisa a qualquer área que requerer dados sobre imigrantes em São Paulo, por exemplo: demandas de transparência ativa e passiva, bem como subsidiando processos técnicos, apresentações institucionais e outros contextos correlatos.

### Encaminhamentos - Botão para cadastrar novo

<figure><img src="../../.gitbook/assets/image (3) (1).png" alt=""><figcaption></figcaption></figure>

Adicionado novo botão para permitir cadastrar novos encaminhamentos a partir da Central de Encaminhamentos.

Até então, o cadastro de novos encaminhamentos era obrigatoriamente feito através do cadastro da pessoa.

### Segurança - Bloqueio de acesso em múltiplos dispositivos

~~Por questões de segurança, a partir desta versão não será mais possível utilizar a mesma conta em dois dispositivos simultaneamente.~~

~~Sempre que for realizado um novo login, o sistema invalidará automaticamente todas as demais sessões abertas do usuário, independentemente do equipamento utilizado.~~

~~Essa medida tem como objetivo prevenir o compartilhamento de senhas.~~

{% hint style="warning" %}
A melhoria acima foi desabilitada na versão 5.0.3 devido a instabilidade no mecanismo.
{% endhint %}

### Transcidadania - Data da suspensão

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

Adicionado novo campo para informar a "Data de início da Suspensão", quando o status for "Suspenso".

Com base nesse campo, os cadastros ficarão automaticamente inconsistentes caso o período de suspensão ultrapasse 90 dias.

<figure><img src="../../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

O sistema também passará a exibir o tipo de inconsistência no próprio registro.

### Transcidadania - Faltas excedidas

Adicionada nova inconsistência caso haja três ou mais ocorrências de falta (frequência total menor que 40%) no período de 12 meses.

### Transcidadania - Pesquisa de pessoas

A pesquisa de pessoas na tela de acompanhamento permitirá agora pesquisar pelo código SIAD, CPF, Nome Civil e Nome Social.

## Ajustes

### Atendimentos - Erro ao limpar data

Corrigido erro que era exibido ao apagar o campo da data do atendimento.

### Atendimentos - Campos de moeda

Corrigida a forma de armazenamento dos campos de tipo "Moeda".

### Encaminhamentos - Registros excluídos

Foi corrigida a exibição de encaminhamentos que haviam sido excluídos, na Central de Encaminhametos.

### Infraestrutura - IPs de acesso

Corrigida a forma de armazenamento dos IPs de usuários no log de acessos do sistema.

### Transcidadania - Sincronização de frequências históricas

Foi desativada a sincronização da frequência com o cadastro ao lançar frequências históricas.

### Hotfixes

Após a publicação da versão, foi necessário realizar alguns ajustes, conforme abaixo:

* v5.0.1 e v5.0.2: correção de erro ao abrir atendimento de imigrantes, por conta de um problema relacionado à checagem no campo de Situação Migratória;
* v5.0.3: remoção temporária do mecanismo de bloqueio de sessões do usuário abertas em outros dispositivos.
