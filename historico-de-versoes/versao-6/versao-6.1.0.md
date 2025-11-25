---
description: 'Data de lançamento (estimada): 25/11/2025'
---

# Versão 6.1.0

A **versão 6.1.0** do SIAD é uma versão que traz o formulário de recursos do Edital Rango Responsa 2025, melhorias no SIAD Projetos e ajustes diversos.

Confira abaixo todos os detalhes dessa atualização.

## Melhorias

### Atendimentos - Impressão do atendimento

<figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

Foi disponibilizado um novo botão na tela de visualização que permite imprimir a ficha de atendimento.

Além disso, foi corrigido um problema que exibia uma página em branco adicional nos impressos de atendimentos e encaminhamentos, nos ambientes de testes.

### Cadasto de Pessoas - Tem Saída

Adicionada nova opção de benefício "Tem Saída", na aba Dados Socioeconômicos.

### CadÚnico - Melhorias na importação

Foi adicionada uma nova etapa de verificação no processo de importação da base do CadÚnico para o SIAD, garantindo maior confiabilidade das informações e evitando erros inesperados decorrentes de eventuais mudanças no formato dos dados.

Além disso, durante a importação, as telas de cadastro de pessoas não serão mais impactadas.

### Edital Rango Responsa 2025

Implementada a fase de recursos do Edital.

### Eleições COMPLIR 2025 (Prévia)

Disponibilizada versão prévia, para testes, do formulário de inscrição das Eleições COMPLIR 2025.

### Encaminhamentos - Filtro de protocolo

Adicionado novo filtro que permite pesquisar encaminhamentos pelo número de protocolo.

### Projetos - Melhorias e ajustes diversos

Foram realizadas as seguintes melhorias e ajustes no SIAD Projetos:

* Nova tela para visualizar etapas pelas quais a área do usuário logado é responsável.
* Aumento do tamanho do nome do projeto para até 90 caracteres.
* O histórico de edições e alterações do projeto passa a exibir agora todas as alterações realizadas no cronograma/etapas.
* O sistema passa a solicitar uma justificativa caso algum dos seguintes campos sejam alterados, no cadastro da etapa: Status, Área Responsável, Data Início ou Data Fim.
* Agora é possível visualizar e restaurar etapas excluídas.
* Implementado novo campo de "Periodicidade de Monitoramento" no cadastro do projeto.
* Foi corrigido um erro que era exibido ao tentar cadastrar um novo projeto caso não houvesse instruções configuradas no SIAD Projetos.
* Foram corrigidas as datas exibidas no histórico de edições de um projeto, que não estavam considerando o fuso horário.
* Corrigido problema ao pesquisar com a tabela agrupada.
* Corrigidos filtros da tela de listagem de projetos que não funcionavam com o perfil de áreas.
* Atualizado texto do critério 5, no cadastro do projeto.

## Ajustes

### Atendimentos - Erro ao consultar com apóstrofe

Foi corrigido um erro que era exibido ao pesquisar com apóstrofe nos termos de pesquisa.

### Atendimentos - Bug ao gravar menor desacompanhado

Foi corrigido um erro que não exibia corretamente o campo "Menor desacompanhado" nos atendimentos de imigrantes.

O campo foi substituído por um novo componente que previnirá futuros erros.

### Atividades Coletivas - Correção de histórico

Corrigido problema que continuava exibindo o registro da atividade no histórico da pessoa caso a mesma fosse excluída de uma atividade existente.

### Cadastro de Equipamentos - Correção de erro no cadastro

Corrigido erro (de redirecionamento) que era exibido ao tentar cadastrar um novo equipamento.

### Cadastro de Pessoas - Correção da transferência de histórico

Corrigido problema que impedia os Administradores de transferirem registros históricos (de atendimentos, encaminhamentos etc.) de cadastros duplicado, após a subida da versão 6.0.
