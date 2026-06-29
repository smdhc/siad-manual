# Construção de Fluxos

## Introdução aos Fluxos

### O que é um Fluxo?

Um **Fluxo** é a estrutura principal de coleta de dados no SIAD Forms. Ele organiza o processo de preenchimento em **etapas sequenciais**, onde cada etapa possui um formulário vinculado. Ao preencher a primeira etapa, o sistema gera um **Protocolo** — um registro identificado por um número único que acompanha todo o ciclo de vida do processo.

Pense no fluxo como um processo de trabalho digitalizado: cada etapa representa um momento distinto de coleta de informações, e o protocolo é o "dossiê" que agrupa todas as respostas ao longo dessas etapas.

### Para que servem?

Fluxos permitem construir processos de coleta de dados que:

* Possuem **múltiplas etapas** com formulários diferentes (ex: inscrição, análise, parecer, devolutiva)
* Controlam **quem pode preencher cada etapa** (por usuário, equipamento, temática ou tipo de equipamento)
* Definem **regras de progressão** baseadas em status do protocolo (ex: a etapa "Análise" só é liberada quando o protocolo está com status "Aguardando análise")
* Oferecem **visibilidade pública ou interna** por etapa — uma etapa pode ser acessível sem login, enquanto outra exige autenticação
* Permitem **acompanhamento** pelo respondente, que pode consultar suas respostas a qualquer momento via número do protocolo
* Suportam **notificações automáticas** por e-mail ou pelo sistema quando eventos ocorrem (nova resposta, alteração de status, exclusão etc.)
* Controlam **edição, exclusão e restauração** de respostas com permissões granulares

### Como funciona a hierarquia

```
Fluxo
├── Configurações Gerais (acesso, status permitidos, restrições, notificações)
├── Versão 1 (rascunho)
│   ├── Etapa 1 - Inscrição (pública, tipo inicial)
│   │   └── Formulário vinculado (versão publicada)
│   ├── Etapa 2 - Análise (interna, tipo intermediária)
│   │   └── Formulário vinculado (versão publicada)
│   └── Etapa 3 - Devolutiva (pública, tipo intermediária)
│       └── Formulário vinculado (versão publicada)
└── Versão 2 (publicada)
    ├── Etapa 1 - Inscrição (...)
    ├── Etapa 2 - Triagem (...)
    ├── Etapa 3 - Análise (...)
    └── Etapa 4 - Devolutiva (...)
```

### Ciclo de vida

O fluxo possui dois níveis de status:

**Status do Fluxo** (nível global):

* **Rascunho** — em construção, não acessível publicamente
* **Publicado** — ativo e acessível conforme as configurações
* **Arquivado** — desativado, não aceita mais respostas

**Status da Versão** (nível da versão):

* **Rascunho** — versão em preparação
* **Publicada** — versão ativa (apenas uma pode estar publicada por vez)
* **Arquivada** — versão inativa

Para que um fluxo esteja funcional, é necessário que o fluxo esteja **Publicado** e que exista uma versão com status **Publicada**.

### O versionamento

O sistema de versões garante a integridade do processo. Versões são necessárias quando há alterações estruturais no fluxo (adicionar/remover etapas, alterar a sequência). Alterações no conteúdo das etapas (textos, layout, atributos dos formulários) não exigem nova versão.

Ao criar uma nova versão, é possível copiar as etapas de uma versão anterior como ponto de partida.

### Protocolos e Respostas

* **Protocolo**: criado automaticamente quando alguém preenche a etapa inicial. Recebe um número sequencial único e um status.
* **Resposta**: dados preenchidos em uma etapa específica de um protocolo. Cada etapa pode ter no máximo uma resposta ativa por protocolo.

### Tipos de etapa

| Tipo              | Comportamento                                                                                   |
| ----------------- | ----------------------------------------------------------------------------------------------- |
| **Inicial**       | Gera um novo protocolo ao ser preenchida. É o ponto de entrada do fluxo.                        |
| **Intermediária** | Exige um número de protocolo existente para ser acessada. Permite dar continuidade ao processo. |

### Visibilidade das etapas

| Visibilidade | Comportamento                                                                |
| ------------ | ---------------------------------------------------------------------------- |
| **Público**  | Qualquer pessoa pode acessar o formulário via URL, sem necessidade de login. |
| **Interno**  | Somente usuários logados com permissão configurada podem acessar.            |

### Perfis de acesso

<table><thead><tr><th width="218.3333740234375">Perfil</th><th width="159.6666259765625">Escopo</th><th>Capacidades</th></tr></thead><tbody><tr><td><strong>Administrador do Sistema</strong></td><td>Global</td><td>Acesso total a todos os fluxos e protocolos</td></tr><tr><td><strong>Administrador do Fluxo</strong></td><td>Por fluxo</td><td>Gerencia etapas, versões e protocolos do fluxo</td></tr><tr><td><strong>Editor do Fluxo</strong></td><td>Por fluxo</td><td>Gerencia status e observações dos protocolos</td></tr><tr><td><strong>Usuário com acesso à Etapa</strong></td><td>Por etapa</td><td>Consultar, cadastrar, alterar, excluir ou reativar respostas conforme permissões</td></tr><tr><td><strong>Usuário Público</strong></td><td>Etapas públicas</td><td>Preenche formulários públicos sem login</td></tr></tbody></table>
