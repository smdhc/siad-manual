---
description: 'Data de lançamento: 16/10/2025'
---

# Versão 5.2.0

A **versão 5.2.0** do SIAD é uma versão que traz <mark style="background-color:blue;">melhorias e ajustes</mark> diversos no sistema em geral.

Confira abaixo todos os detalhes dessa atualização.

## Melhorias

### Laravel 11

O framework utilizado para o desenvolver o SIAD foi atualizado da versão 10 para a versão 11, trazendo melhorias importantes em desempenho, segurança e estabilidade. Essa nova versão torna o ambiente mais moderno e eficiente e representa um primeiro passo para atualizar os demais componentes do sistemas. Nenhuma mudança visual foi feita — tudo continua funcionando como antes, mas com uma base mais leve, segura e preparada para futuras evoluções.

## Ajustes

### Cidade Solidária - Melhorias e ajustes

Foram realizados os seguintes ajustes no módulo do Programa Cidade Solidária:

* Correção de erro ao pesquisar remessa emergencial pela pesquisa global;
* Correção de erro ao tentar cadastrar remessa sem ter um ciclo vigente;
* Correção de erro ao gravar remessa (entidade);
* Correção de erro ao consultar credencial expirada;
* Inclusão e atualização de mensagens explicativas no cadastro da remessa;
* Bloqueio da edição do e-mail da entidade no cadastro da remessa.

### Edital Rango Responsa - Correção de submissão de formulário

O formulário do Edital Rango Responsa 2025 foi ajustado para impedir a submissão ao pressionar a tecla **Enter**, evitando, assim, erros que vinham ocorrendo anteriormente.

### Transcidadania - Correção na exibição do nome da escola

Corrigido cenário em que houve alteração de rede escolar (particular para municipal, por exemplo) e o nome da escola não estava sendo atualizado.
