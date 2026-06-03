# Criar uma versão

Toda a estrutura de seções e campos fica dentro de uma versão. Um formulário recém-criado não possui versões, portanto o próximo passo é criar a primeira.

## Como acessar

1. Na sidebar do formulário, clique em **Versões**
2. Clique no botão **Cadastrar Versão**

<figure><img src="../../.gitbook/assets/image (224).png" alt=""><figcaption></figcaption></figure>

## Campos do cadastro

<table><thead><tr><th width="172">Campo</th><th width="162">Obrigatório</th><th>Descrição</th></tr></thead><tbody><tr><td><strong>Versão</strong></td><td>Sim (automático)</td><td>Número sequencial gerado automaticamente (1, 2, 3...). Não é editável.</td></tr><tr><td><strong>Status</strong></td><td>Sim (automático)</td><td>Novas versões sempre iniciam como <strong>Rascunho</strong>.</td></tr><tr><td><strong>Copiar dados da versão</strong></td><td>Não</td><td>Permite copiar todas as seções e atributos de uma versão anterior. Útil ao criar uma nova versão com pequenas alterações em relação à anterior. Será exibindo somente quando já houver outra versão cadastrada.</td></tr><tr><td><strong>Permitir visualização</strong></td><td>Não</td><td>Habilita a prévia da versão para revisão antes da publicação.</td></tr><tr><td><strong>Observações</strong></td><td>Não</td><td>Texto livre para registrar o motivo da nova versão ou alterações realizadas.</td></tr></tbody></table>

<figure><img src="../../.gitbook/assets/image (225).png" alt=""><figcaption></figcaption></figure>

## Status da versão

Uma versão do formulário passa por um ciclo de vida bem definido:

<table><thead><tr><th width="142">Status</th><th width="426">Significado</th><th>Pode ser editada?</th></tr></thead><tbody><tr><td><strong>Rascunho</strong></td><td>Versão em construção. Seções e atributos podem ser criados, editados e removidos livremente, contudo, o formulário ainda fica inacessível.</td><td>Sim</td></tr><tr><td><strong>Publicada</strong></td><td>Versão definitiva, disponível para vinculação a etapas de fluxos e no SIAD Benefícios.</td><td>Não</td></tr><tr><td><strong>Arquivada</strong></td><td>Versão descontinuada. Não pode ser editada nem vinculada a novas etapas.</td><td>Não</td></tr></tbody></table>

**Regras importantes:**

* Só pode existir **uma versão publicada** por formulário a cada momento.
* Ao publicar uma nova versão, a versão publicada anterior é **arquivada automaticamente**.
* Uma versão arquivada pode voltar ao status "Publicada" somente se não houver outra versão publicada no momento.
* Versões vinculadas a etapas de fluxo não podem ser arquivadas manualmente.

{% hint style="warning" %}
**Atenção:** ao publicar uma nova versão de formulário, é necessário atualizar manualmente as etapas que fazem uso do formulário para a nova versão.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (226).png" alt=""><figcaption></figcaption></figure>

A partir desse ponto, já é possível começar a construir as seções e atributos do formulário, clicando no botão "**Seções**" da versão desejada.
