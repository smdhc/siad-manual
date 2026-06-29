# Gerenciar Versões

## Introdução

O sistema de versões garante a integridade e a rastreabilidade do fluxo. Cada versão contém sua própria estrutura de etapas, permitindo evoluir o processo sem afetar protocolos já criados em versões anteriores.

Para acessar o gerenciamento de versões, navegue até **SIAD Forms > Fluxos**, selecione o fluxo desejado e clique na aba **Versões** na sub-navegação.

***

## Quando criar uma nova versão

Uma nova versão é **necessária** quando há alterações na **estrutura** do fluxo:

* Adição de novas etapas
* Remoção de etapas existentes
* Alteração da sequência ou do funcionamento entre etapas

Uma nova versão **não é necessária** para:

* Edição de textos e instruções dentro das etapas
* Ajustes de layout ou organização visual
* Atualização de descrições e orientações
* Alteração de atributos ou configurações dos formulários vinculados
* Modificação de permissões de acesso nas etapas

***

## Criar uma versão

Clique no botão **Cadastrar Nova Versão** no topo da listagem. O modal de criação contém:

<table><thead><tr><th width="193.6666259765625">Campo</th><th width="143" align="center">Obrigatório</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Versão</strong></td><td align="center">Sim</td><td>Número sequencial atribuído automaticamente pelo sistema (1, 2, 3...). Não editável.</td></tr><tr><td><strong>Status</strong></td><td align="center">Sim</td><td>Sempre inicia como <strong>Rascunho</strong>. Não pode ser alterado na criação.</td></tr><tr><td><strong>Copiar dados da versão</strong></td><td align="center">Não</td><td>Permite copiar todas as etapas (e suas configurações) de uma versão existente para a nova. Útil para evitar recriação manual quando a alteração é incremental.</td></tr><tr><td><strong>Observações</strong></td><td align="center">Não</td><td>Texto livre para registrar o motivo da criação da versão ou quais alterações foram realizadas.</td></tr></tbody></table>

Ao confirmar, a versão é criada e suas etapas podem ser configuradas.

***

## Ciclo de vida da versão

As versões seguem um fluxo linear de status:

```
Rascunho → Publicada → Arquivada
                ↑           │
                └───────────┘ (pode reativar se não houver outra publicada)
```

<table><thead><tr><th width="131">Status</th><th width="291">Significado</th><th align="center">Pode editar etapas?</th><th align="center">Acessível publicamente?</th></tr></thead><tbody><tr><td><strong>Rascunho</strong></td><td>Em preparação. Etapas sendo configuradas.</td><td align="center">Sim</td><td align="center">Não</td></tr><tr><td><strong>Publicada</strong></td><td>Versão ativa do fluxo. Protocolos novos serão criados nesta versão.</td><td align="center">Não</td><td align="center">Sim (se o fluxo estiver publicado)</td></tr><tr><td><strong>Arquivada</strong></td><td>Versão inativa. Protocolos existentes mantêm vínculo histórico.</td><td align="center">Não</td><td align="center">Não</td></tr></tbody></table>

### **Regras de transição**

* **Rascunho → Publicada**: ao publicar uma versão, o sistema automaticamente **arquiva** qualquer outra versão que estivesse publicada. Apenas uma versão pode estar publicada por vez.
* **Publicada → Arquivada**: desativa a versão. Se o fluxo não tiver outra versão publicada, ficará sem versão ativa (e não será acessível publicamente).
* **Arquivada → Publicada**: só é permitido se não houver outra versão atualmente publicada. Permite reativar uma versão anterior.

***

## Alterar o status de uma versão

Para alterar o status, clique no botão de **edição** (ícone de lápis) na linha da versão desejada. O campo **Status** exibirá apenas as transições válidas de acordo com o estado atual:

* Se a versão está em Rascunho: opções serão Rascunho ou Publicada
* Se está Publicada: opções serão Publicada ou Arquivada
* Se está Arquivada: opção será Publicada (somente se não existir outra publicada)

O helper text abaixo do campo explica o efeito de cada status:

* _Rascunho_: "Versão inicial, ainda não poderá ser utilizada."
* _Publicada_: "Versão definitiva, disponível para utilização. Uma vez publicada, não poderá mais ser editada e irá arquivar outras versões publicadas automaticamente."
* _Arquivada_: "Fluxos ativos deixam de ser exibidos, não pode ser editada. Novas versões publicadas automaticamente arquivam versões publicadas."

***

## Gerenciar etapas da versão

Na listagem de versões, cada linha possui o botão **Etapas** (ícone de retângulos empilhados) que leva à tela de gerenciamento de etapas daquela versão específica.

Esse é o próximo passo após criar a versão: definir quais etapas comporão o fluxo, quais formulários serão utilizados e como será o controle de acesso e progressão.

***

## Copiar uma versão existente

Ao criar uma nova versão, o campo **Copiar dados da versão** permite selecionar uma versão anterior. Ao fazer isso, todas as etapas da versão de origem serão duplicadas para a nova, incluindo:

* Nome e configurações gerais de cada etapa
* Formulário e versão vinculados
* Configurações de acesso
* Configurações de prazo
* Configurações de notificações

Após a cópia, as etapas podem ser livremente editadas, adicionadas ou removidas na nova versão sem impacto na versão de origem.

***

## Excluir uma versão

Versões podem ser excluídas pelo botão de exclusão na listagem. A exclusão é um soft delete (reversível).

> **Atenção**: excluir uma versão que possui protocolos vinculados pode afetar a consulta histórica desses protocolos. Prefira arquivar em vez de excluir.

***

## Boas práticas

* Mantenha o campo **Observações** preenchido com o motivo da nova versão para facilitar a rastreabilidade futura.
* Antes de publicar uma nova versão, certifique-se de que todas as etapas estão configuradas e que os formulários vinculados possuem versões publicadas.
* Utilize a funcionalidade de cópia para agilizar a criação de versões incrementais.
* Evite excluir versões com protocolos vinculados — arquive-as.
