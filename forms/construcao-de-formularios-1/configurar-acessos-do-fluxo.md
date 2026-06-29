# Configurar acessos do fluxo

## Introdução

As configurações de acesso definem quem pode gerenciar o fluxo e seus protocolos. Essa configuração fica na seção **Configurações de Acesso** ao editar um fluxo (menu lateral SIAD Forms > Fluxos > selecionar o fluxo > Editar).

> **Importante**: as permissões configuradas aqui se referem ao **gerenciamento do fluxo e dos protocolos**, e não ao preenchimento dos formulários. O acesso para preenchimento é configurado individualmente em cada etapa.

***

## Entendendo os perfis

O SIAD Forms trabalha com uma hierarquia de perfis de acesso:

<table><thead><tr><th width="185">Perfil</th><th width="213.6666259765625">Escopo</th><th>O que pode fazer</th></tr></thead><tbody><tr><td><strong>Administrador do Sistema</strong></td><td>Global (automático)</td><td>Acesso irrestrito a todos os fluxos, versões, etapas e protocolos. Não precisa ser configurado.</td></tr><tr><td><strong>Administrador do Fluxo</strong></td><td>Por fluxo (configurável)</td><td>Gerencia versões e etapas do fluxo. Pode excluir e restaurar protocolos. Não é afetado por restrições de acesso às respostas.</td></tr><tr><td><strong>Editor do Fluxo</strong></td><td>Por fluxo (configurável)</td><td>Pode alterar o status e as observações dos protocolos. Não é afetado por restrições de acesso às respostas. Não pode excluir protocolos.</td></tr></tbody></table>

A diferença principal entre Administrador e Editor:

* O **Administrador** tem controle total sobre a estrutura do fluxo (criar/editar versões e etapas) e pode excluir/restaurar protocolos.
* O **Editor** atua apenas na operação dos protocolos (mudar status, adicionar observações), sem poder alterar a configuração do fluxo nem excluir protocolos.

***

### Como configurar

Na seção **Configurações de Acesso**, clique em **Adicionar nova permissão**. Cada linha representa uma regra de acesso composta por três campos:

**Tipo de entidade**

Define a quem o acesso será concedido:

<table><thead><tr><th width="210">Tipo</th><th>Comportamento</th></tr></thead><tbody><tr><td><strong>Usuário</strong></td><td>Concede acesso a um ou mais usuários específicos, identificados por nome, e-mail ou CPF.</td></tr><tr><td><strong>Equipamento</strong></td><td>Concede acesso a todos os usuários vinculados aos equipamentos selecionados.</td></tr><tr><td><strong>Temática</strong></td><td>Concede acesso a todos os usuários de equipamentos pertencentes às temáticas selecionadas.</td></tr><tr><td><strong>Tipo de Equipamento</strong></td><td>Concede acesso a todos os usuários de equipamentos dos tipos selecionados.</td></tr></tbody></table>

### **Seleção da entidade**

O campo central se adapta ao tipo escolhido:

* **Usuário**: busca por nome, e-mail ou CPF. Exibe o equipamento do usuário entre parênteses para facilitar a identificação.
* **Equipamento**: lista com busca dos equipamentos cadastrados.
* **Temática**: lista com busca das temáticas disponíveis.
* **Tipo de Equipamento**: lista com busca dos tipos de equipamento.

Em todos os casos, é possível selecionar múltiplos registros na mesma regra.

**Tipo de Acesso**

<table><thead><tr><th width="167.333251953125">Opção</th><th>Capacidades</th></tr></thead><tbody><tr><td><strong>Administrador</strong></td><td>Criar/editar versões e etapas. Visualizar todos os protocolos (sem restrição). Excluir e restaurar protocolos. Alterar status.</td></tr><tr><td><strong>Editor</strong></td><td>Visualizar todos os protocolos (sem restrição). Alterar status e observações dos protocolos.</td></tr></tbody></table>

***

### Combinando múltiplas regras

É possível (e comum) adicionar várias regras para atender diferentes cenários. As regras são avaliadas de forma independente — basta que o usuário se encaixe em ao menos uma regra para ter o acesso correspondente.

**Exemplo prático — Fluxo de Inscrição em Programa Social:**

<table><thead><tr><th width="96.3333740234375">Regra</th><th width="169">Tipo</th><th>Entidade</th><th>Tipo de Acesso</th></tr></thead><tbody><tr><td>1</td><td>Usuário</td><td>Maria Silva, João Oliveira</td><td>Administrador</td></tr><tr><td>2</td><td>Equipamento</td><td>CRCM ABC, CRCM XYZ</td><td>Editor</td></tr><tr><td>3</td><td>Temática</td><td>Mulheres</td><td>Editor</td></tr></tbody></table>

Neste cenário:

* Maria e João podem configurar o fluxo, criar versões, gerenciar etapas e excluir protocolos.
* Todos os profissionais do CRCM ABC e CRCM XYZ podem alterar status e observações dos protocolos.
* Todos os profissionais de qualquer equipamento da temática Mulheres também podem atuar como Editores.

***

## Quem aparece na listagem de fluxos

O acesso configurado aqui também define quem pode **ver o fluxo** na listagem do módulo Forms. Apenas os seguintes perfis visualizam um fluxo na tela de gerenciamento:

* Administradores do Sistema (veem todos)
* Usuários com pelo menos uma regra de acesso do tipo **Administrador** naquele fluxo

Editores do fluxo **não** veem o fluxo na listagem de fluxos — eles atuam diretamente nos protocolos via a tela de gerenciamento de protocolos.

***

## Efeito sobre restrições de acesso

Tanto Administradores quanto Editores do fluxo **não são afetados** pelas seguintes restrições:

* Restrição de acesso aos protocolos (configurada nos Dados Gerais do fluxo)
* Restrição de visualização de respostas por etapa (configurada na etapa)

Isso significa que, independentemente dessas configurações, Administradores e Editores sempre poderão ver todos os protocolos e todas as respostas do fluxo.

***

## Quando configurar

As configurações de acesso podem ser definidas no momento da criação do fluxo ou ajustadas posteriormente a qualquer momento. Não é necessário ter o fluxo publicado para testar os acessos — basta que o usuário acesse o módulo de protocolos internamente.

Caso nenhum acesso seja configurado, apenas Administradores do Sistema poderão gerenciar o fluxo.
