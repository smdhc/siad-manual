---
description: 'Data de lançamento: 19/09/2024'
---

# Versão 1.1.0

A versão 1.1.0 do SIAD traz uma série de melhorias e novas funcionalidades com base nos feedbacks recebidos ao longo do [projeto piloto](../../introducao/projeto-piloto.md), tendo como destaque a nova funcionalidade de Relatórios e melhorias diversas no módulo de [Encaminhamentos](../../pessoas/encaminhamentos.md).

## Novas funcionalidades

### Relatórios

<figure><img src="../../.gitbook/assets/image (11) (1) (1) (1).png" alt=""><figcaption><p>Nova funcionalidade de relatórios</p></figcaption></figure>

Foi implementada uma nova funcionalidade de Relatórios, disponível como nova opção no menu lateral do sistema, que servirá como principal forma de exportar relatórios e planilhas diversos do sistema.

Nessa versão foram disponibilizados dois novos relatórios:

* **Relatório Consolidado de Pessoas Cadastradas por Equipamento**\
  Permite exportar uma planilha que contabiliza o total de cadastros realizados por equipamento e por mês de cadastro.
* **Relatório de Equipamentos**\
  Permite exportar a relação completa de equipamentos da SMDHC.

## Melhorias

### Formatação de Encaminhamentos

Foram adicionadas novas opções de formatação nos encaminhamentos, permitindo assim controlar o tamanho do texto e demais opções de formatação de texto.

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>Formatação dos encaminhamentos</p></figcaption></figure>

### Novo indicador de pessoas cadastradas na rede

No Painel de Controle, foi adicionado um novo indicador contendo o total de pessoas cadastradas em todos os equipamentos da rede de atendimento da SMDHC.

<figure><img src="../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>Indicador de pessoas cadastradas na rede</p></figcaption></figure>

### Novos filtros de pesquisa de pessoas

Nos filtros da tela de pesquisa do Cadastro de Pessoas, foram adicionadas duas novas opções que permitem filtrar cadastros que possuem Composição Familiar e Encaminhamentos.

<figure><img src="../../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>Novos filtros no cadastro de pessoas</p></figcaption></figure>

### Filtro padrão de pessoas cadastradas no equipamento

A partir dessa versão, ao entrar no Cadastro de Pessoas, serão exibidos por padrão somente os cadastros do equipamento (ao invés de exibir todos os cadastros da rede DH).

### Atualização de texto do campo Observações

Observamos que o sistema não deixa claro para o usuário que, após o preenchimento de um novo cadastro, há outras seções disponíveis para adicionar informações, como números de prontuários existentes, composição familiar e encaminhamentos. Devido a essa falta de clareza, muitos usuários acabavam inserindo essas informações de forma inadequada no campo inicial.

Para solucionar essa questão, atualizamos o texto de orientação, esclarecendo aos novos usuários que esse campo não deve ser utilizado para essas finalidades.

<figure><img src="../../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>Texto explicativo do campo "Observações"</p></figcaption></figure>

### Texto de usuário/senha inválidos

O texto exibido na tela de login, ao tentar acessar o sistema com credenciais inválidas, foi aprimorado para comunicar de forma mais clara o motivo do erro ao usuário.

<figure><img src="../../.gitbook/assets/image (7) (1) (1) (1) (1).png" alt=""><figcaption><p>Texto exibido no caso de credenciais inválidas</p></figcaption></figure>

### Vigência de Equipamentos

Foram adicionados dois novos campos de vigência no Cadastro de Equipamentos, permitindo a desativação de equipamentos que atualmente não estão em funcionamento.

O acesso à edição desses campos está restrito aos administradores do sistema.

<figure><img src="../../.gitbook/assets/image (9) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>Campos de vigência do equipamento</p></figcaption></figure>

### Filtros no cadastro de usuários

Foram adicionados novos filtros de pesquisa ao cadastro de usuários. O acesso à essa funcionalidade está restrita aos administradores do sistema.

<figure><img src="../../.gitbook/assets/image (10) (1) (1) (1) (1).png" alt=""><figcaption><p>Filtros de pesquisa de usuários</p></figcaption></figure>

## Correções

### Correção do filtro "Realiza Atendimentos" de equipamentos

Foi corrigido o filtro de pesquisa de equipamentos "Realiza atendimentos", que não estava funcionando corretamente, no Cadastro de Equipamentos.

<figure><img src="../../.gitbook/assets/image (11) (1) (1) (1) (1).png" alt=""><figcaption><p>Filtro "Realiza Atendimentos?"</p></figcaption></figure>

### Correção da exibição do Nome Social

Foi corrigida a exibição do <mark style="background-color:purple;">Nome Social</mark> no menu lateral da Ficha de Cadastro da Pessoa, que anteriormente estava exibindo erroneamente o <mark style="background-color:purple;">Nome Civil</mark>.

<figure><img src="../../.gitbook/assets/image (12) (1) (1) (1).png" alt=""><figcaption><p>Exibição do nome social na ficha de cadastro</p></figcaption></figure>

### Correção no cadastro de prontuários

Foi corrigido um bug na associação de prontuários que, ao excluir um prontuário, o número em questão não poderia ser utilizado novamente.

<figure><img src="../../.gitbook/assets/image (13) (1) (1) (1).png" alt=""><figcaption><p>Associação de prontuários</p></figcaption></figure>
