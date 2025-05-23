---
description: 'Data de lançamento: 22/05/2025'
---

# Versão 4.3.0

A **versão 4.3.0** do SIAD é uma versão que traz <mark style="background-color:yellow;">novas funcionalidades</mark> como o **Selo de Igualdade Racial 2025 (prévia) e Virada Cultural 2025**, além de <mark style="background-color:blue;">ajustes</mark> e <mark style="background-color:green;">melhorias</mark> diversas no sistema em geral.

Confira abaixo todos os detalhes dessa atualização.

## Novas funcionalidades

### Selo de Igualdade Racial 2025 - Versão preliminar

Foi disponibilizado um novo formulário público (protótipo) para as inscrições do Programa Selo de Igualdade Racial 2025.

Trata-se de uma versão preliminar, que ainda passará por ajustes e melhorias.

### Virada Cultural 2025

Foi disponibilizado um novo formulário público para o registro das ações de promoção e defesa de direitos humanos na Virada Cultural 2025, que ocorrerá nos dias 24 e 25 de maio.

## Melhorias

### Atendimentos - Cadastro de Profissionais do Equipamento

Foi adicionada uma nova configuração no Cadastro de Usuários para indicar se um usuário é profissional do equipamento.

Com base nessa configuração, a lista de profissionais no registro de atendimentos passará a exibir somente os profissionais que efetivamente trabalham no equipamento (usuários da SMDHC, por exemplo, deixarão de ser exibidos).

### Atendimentos - Novas opções de validação

Foram adicionadas novas configurações de validação em campos numéricos (maior/menor que) e exceção de obrigatoriedade com base em certas condições.

### Cadastro de Pessoas - Novas opções de escolaridade

Foram adicionadas as opções "<mark style="background-color:purple;">Mestrado</mark>" e "<mark style="background-color:blue;">Doutorado</mark>" no rol de opções de Escolaridade, do Cadastro de Pessoas.

### Módulo Admin - Modo noturno

Habilitada a possibilidade de configurar o tema noturno do SIAD no módulo Admin.

Até a próxima versão será avaliado o impacto no sistema para que possamos habilitar nos demais módulos.

## Ajustes

### Cadastro de Pessoas - Correção de CEP sem endereço

Aplicada correção para não armazenar mais em cache CEPs que não retornaram nenhum endereço.

### Cadastro de Pessoas - Correção de edição com RNE (Versão 4.3.1)

Corrigida a validação que impedia alterar um cadastro com RNE, acusando que o mesmo já estava em uso.

### RCC - Correção de erro ao cadastrar restaurantes e pontos de entrega

Aplicada correção no cadastro de restaurantes e pontos de entrega por problema ocasionado na implementação do preenchimento de CEP/Distrito automático da versão 4.2.0.
