# Publicar o Fluxo

### Introdução

Após configurar o fluxo, suas versões e etapas, é necessário publicá-lo para que os formulários fiquem acessíveis aos respondentes. A publicação envolve dois níveis: a **versão** e o **fluxo** em si.

***

## Checklist pré-publicação

Antes de publicar, verifique se todos os itens abaixo estão atendidos:

* [ ] **Formulários com versão publicada**: cada etapa deve estar vinculada a um formulário que possua uma versão com status "Publicada". Caso contrário, o formulário não será renderizado.
* [ ] **Etapa inicial configurada**: o fluxo precisa de pelo menos uma etapa do tipo "Inicial" para que protocolos possam ser gerados.
* [ ] **Slug definido nas etapas públicas**: toda etapa com visibilidade "Público" precisa ter um slug configurado na aba Identificação. Sem slug, a URL não será gerada.
* [ ] **Status cadastrados**: o fluxo precisa ter pelo menos um status configurado em "Status permitidos para as respostas" (nos Dados Gerais). Sem isso, a criação de protocolos falhará.
* [ ] **Permissões de acesso**: para etapas internas, verifique se as regras de acesso estão configuradas. Etapas internas sem regras de acesso serão acessíveis apenas por Administradores do Sistema e do Fluxo.
* [ ] **Pré-requisitos de status coerentes**: se etapas intermediárias possuem pré-requisito de status, certifique-se de que alguma etapa anterior atribui esse status ao ser respondida.

***

## Passo 1: Publicar a versão

A versão é quem contém as etapas. Para publicá-la:

### **Opção A — Pela tela de etapas:**

1. Acesse a versão desejada (SIAD Forms > Fluxos > selecionar o fluxo > Versões > clicar em "Etapas")
2. Clique no botão **Publicar** no topo da listagem de etapas
3. Confirme no modal de confirmação

### **Opção B — Pela listagem de versões:**

1. Acesse SIAD Forms > Fluxos > selecionar o fluxo > aba Versões
2. Clique no ícone de edição (lápis) na linha da versão
3. Altere o campo Status de "Rascunho" para "Publicado"
4. Salve

Ao publicar uma versão, qualquer outra versão que estivesse publicada será **automaticamente arquivada**. Apenas uma versão pode estar publicada por vez.

> **Atenção**: após a publicação, a versão não pode mais ser editada (criação/remoção de etapas fica bloqueada). As configurações internas das etapas (permissões, notificações, regras de fluxo) ainda podem ser ajustadas.

***

## Passo 2: Publicar o fluxo

Com a versão publicada, é hora de ativar o fluxo:

1. Acesse SIAD Forms > Fluxos > selecionar o fluxo > **Editar**
2. Na seção Dados Gerais, altere o campo **Status** de "Rascunho" para **"Publicado"**
3. Salve

A partir deste momento, as etapas públicas estarão acessíveis pelas suas respectivas URLs.

***

## Testar a URL pública

Após a publicação, as etapas públicas ficam acessíveis em:

```
https://siad.prefeitura.sp.gov.br/forms/{slug-da-etapa}
```

Para etapas intermediárias, o acesso exige o parâmetro de protocolo:

```
https://siad.prefeitura.sp.gov.br/forms/{slug-da-etapa}?p={numero-do-protocolo}
```

Você pode acessar a URL diretamente pela listagem de etapas: na coluna **Slug**, o link fica clicável (com ícone de link externo) quando o fluxo e a versão estão publicados. Também é possível usar a ação **Ir para o formulário** no menu de ações da etapa.

### **Verificações recomendadas após publicação**

1. **Acessar a etapa inicial** pela URL pública e preencher o formulário completo para gerar um protocolo de teste
2. **Verificar se o status correto** foi atribuído ao protocolo
3. **Testar etapas intermediárias** usando o número do protocolo gerado
4. **Testar o acompanhamento** (se habilitado) informando o número do protocolo na tela da etapa
5. **Validar as permissões** acessando com usuários de diferentes perfis para confirmar que as restrições funcionam
6. **Verificar notificações** confirmando que os destinatários receberam os alertas configurados

***

## Ciclo resumido

```
1. Criar Fluxo (status: Rascunho)
2. Criar Versão (status: Rascunho)
3. Criar Etapas na versão
4. Publicar Versão → status muda para "Publicada"
5. Publicar Fluxo → status muda para "Publicado"
6. ✅ Formulários acessíveis pelas URLs públicas
```

***

## Despublicar ou suspender temporariamente

Se for necessário suspender o acesso ao fluxo:

* **Arquivar o fluxo** (Status → Arquivado): bloqueia todo acesso público. Protocolos existentes são preservados e podem ser consultados internamente.
* **Arquivar a versão**: mantém o fluxo publicado, mas sem versão ativa. O acesso público retornará erro de "não encontrado".
* **Ajustar datas de disponibilidade**: para suspensão temporária de etapas específicas sem afetar o restante do fluxo, configure a data fim na aba "Regras de Fluxo" da etapa.

Em todos os casos, os dados já coletados (protocolos e respostas) permanecem intactos e consultáveis pelo painel interno.
