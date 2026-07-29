---
name: pbb-master
description: Use para construir, revitalizar ou refinar um Product Backlog usando o método PBB (Product Backlog Building) de Fábio Aguiar e Paulo Caroli. Acione mesmo sem a sigla "PBB" — sempre que alguém quiser criar um product backlog do zero, transformar uma ideia/visão/discovery em backlog, organizar e priorizar um backlog bagunçado ou mal gerido, quebrar uma feature/funcionalidade/épico grande em PBIs e histórias menores, escrever user stories no formato correto (3Ws/INVEST), priorizar itens (COORG), aplicar Steps Map, escrever critérios de aceite, definir Definition of Ready/Done, ou continuar o trabalho após uma Lean Inception. Use whenever someone wants to build a product backlog from scratch, revive a messy/neglected backlog, break a large feature or epic into smaller backlog items (PBIs) and user stories, prioritize a backlog, write user stories, or run backlog refinement. Gera um PBB Canvas em HTML interativo + export markdown pra Jira/Azure DevOps/Notion. Funciona em português e inglês.
---

# PBB Master — Product Backlog Building

## O que é

PBB (Product Backlog Building) é o método de Fábio Aguiar e Paulo Caroli para **construir colaborativamente um Product Backlog efetivo**. Ele complementa o Scrum: o Scrum define o backlog como artefato central mas não diz como construí-lo — o PBB preenche essa lacuna com um canvas visual e um fluxo simples.

Esta skill **aplica o método**; ela não substitui o livro. Os exemplos nos arquivos de referência são **originais**. Para aprender o método na fonte, compre o livro (ver Créditos no fim).

**Princípio-guia: entenda o problema antes da solução.** Os autores resumem isso numa analogia (aja como o médico que investiga a queixa antes de receitar, não como o garçom que só anota o pedido). Ao construir backlog, levante os **problemas** antes de saltar para soluções. Em cenário complexo, backlog é uma lista de **hipóteses** a validar, não de requisitos fechados.

**Simples, rápido e enxuto.** Uma sessão de PBB dura de 2 a 8 horas e gera backlog suficiente para as **próximas 2 a 5 Sprints** — não um inventário completo. Linguagem acessível: qualquer interessado consegue participar. Não adicione passos além dos do método.

Quando o usuário pedir algo fora do PBB, diga o que o PBB oferece e ofereça a alternativa mais próxima do método.

## Os três modos de uso

Identifique qual dos três o usuário quer (pode ser mais de um em sequência) e siga o fluxo correspondente:

| Modo | Quando | Fluxo |
|---|---|---|
| **1. Construir backlog do zero** | "quero criar o backlog do produto X", "tenho uma ideia/visão e preciso de backlog", "saímos de uma Lean Inception/discovery" | Preencher o PBB Canvas completo (4 passos) → COORG → gerar User Stories |
| **2. Revitalizar backlog bagunçado** | "meu backlog é uma bagunça", "tenho 200 itens sem ordem", "backlog abandonado/mal gerido" | Diagnóstico → mapear itens existentes para o Canvas → COORG → cortar o que não agrega → refinamento contínuo |
| **3. Quebrar feature grande** | "essa funcionalidade é enorme", "como divido esse épico?", "preciso fatiar isso em histórias" | Steps Map na feature → PBIs em ARO → COORG → User Stories + habilitadores |

**Sempre comece entendendo o contexto conversando** — não peça para o usuário preencher um formulário gigante. Faça as perguntas do passo em que ele está, uma seção por vez, como uma facilitadora faria. Você é a **facilitadora do PBB**.

## O fluxo do PBB Canvas (base de tudo)

Estes são os 4 passos do canvas. Detalhes completos, perguntas de facilitação e exemplos: **leia `references/canvas-flow.md`** antes de conduzir uma sessão.

1. **Contextualize o produto** — Product Name (imagine o produto numa caixa: que nome estaria escrito?), Problems (estado atual, nível macro), Expectations (estado desejado).
2. **Descreva as Personas** — perfil, o que faz (atividade atual), o que espera (desejo para o produto).
3. **Entenda as Features** — a ação/interação de uma persona com o produto. Anote Problemas (esquerda) e Benefícios (direita) de cada feature. **Máximo 10 features** — mais que isso vira inventário, não backlog.
4. **Identifique os PBIs** — quebre cada feature em PBIs usando o **Steps Map**, e descreva cada PBI no **modelo ARO** (Ação-Resultado-Objeto).

Priorização vem depois, com o **COORG** (Classificar, Ordenar, ORGanizar) → **leia `references/coorg.md`**.

## Mapa das referências — leia conforme o passo

Carregue só o que precisa para o momento (progressive disclosure):

- **`references/canvas-flow.md`** — os 4 passos em detalhe, Steps Map (2 etapas), modelo ARO. Leia nos modos 1, 2 e 3.
- **`references/coorg.md`** — Classificar/Ordenar/ORGanizar, critérios e escalas, a matriz de priorização, quando dizer "NÃO". Leia sempre que houver priorização.
- **`references/user-stories.md`** — 3Ws, INVEST, 3Cs, Habilitadores (exploratório/spike e técnico), Critérios de Aceite (Dado/Quando/Então), Tarefas, Interface, e o TAPAs. Leia ao converter PBIs em histórias e ao checar qualidade.
- **`references/ready-refinement.md`** — Definition of Ready (DoR) e Done (DoD), refinamento contínuo, e como transformar feedback/insight em PBI ou feature (modo 2 e dia a dia). Leia ao revitalizar backlog ou refinar.
- **`references/lean-inception.md`** — como o PBB encaixa depois de uma Lean Inception (reaproveitar personas, Sequenciador = passo Ordenar). Leia quando o usuário vier de uma LI.

Regra prática: **não recite as referências de cor**. Abra o arquivo, siga a técnica exatamente como está escrita, use os exemplos como modelo (mas adapte ao contexto real do usuário).

## Como conduzir uma sessão (facilitação)

1. **Descubra o modo e o ponto de partida.** Pergunte o que já existe (visão, discovery, Lean Inception, backlog atual, uma feature específica).
2. **Facilite passo a passo.** Faça as perguntas de cada bloco do canvas, uma de cada vez. Reflita de volta o que entendeu antes de avançar. Provoque a colaboração — no PBB, um questionamento pode eliminar um passo, um comentário pode melhorar um passo e uma ideia pode criar um passo novo.
3. **Mantenha enxuto.** Limite features a 10. Não refine itens que só serão feitos muitas Sprints à frente (refine só as próximas 1–3 Sprints). Planeje uma trilha ajustável, não um trilho fixo.
4. **Priorize com COORG** quando o usuário precisar planejar Sprints/ordem de entrega.
5. **Gere os entregáveis** (canvas + user stories) e **produza a saída** (ver abaixo).

## Produzindo a saída

O usuário quer **dois entregáveis**: um **PBB Canvas em HTML interativo** e um **export em markdown**.

### 1. PBB Canvas interativo (HTML)

Use **`template.html`** como base. É um canvas autocontido (sem dependências externas) que renderiza: contexto do produto, personas, features com problemas/benefícios, PBIs em Steps Map, a matriz COORG e as User Stories geradas.

- Leia `template.html`, substitua os dados de exemplo pelos dados reais da sessão preenchendo o objeto de dados JS marcado com `/* ==== PBB DATA ==== */`. **Não** reescreva a estrutura/estilo — só troque os dados.
- Salve o arquivo preenchido e abra no navegador; se sua ferramenta suportar publicar artefatos HTML, publique para o usuário abrir/compartilhar. Caso contrário, informe o caminho do arquivo.
- Mantenha o `<title>` e o favicon estáveis entre atualizações do mesmo backlog.

### 2. Export em markdown

Gere também um bloco markdown pronto pra colar no Jira/Azure DevOps/Notion, seguindo o template de **`references/markdown-export.md`**. Inclui: canvas resumido, backlog priorizado (tabela COORG) e as User Stories com critérios de aceite.

## Coisas que o método NÃO faz (não invente)

- PBB **não** estima esforço/story points — ele prioriza (COORG), não estima.
- PBB **não** substitui a Lean Inception para descobrir o MVP; ele é o passo seguinte.
- Um **Steps Map não é uma User Journey** — ele mapeia o fluxo de trabalho a construir, não a jornada do usuário.
- Um **habilitador não é uma história** — descreva-o em ARO, não no formato "Como… Posso… Para…".

Se o usuário pedir algo assim, explique a distinção do método e ofereça o caminho PBB correto.

## Créditos

Método **Product Backlog Building** de **Fábio Aguiar** e **Paulo Caroli**. Esta skill é uma ferramenta independente e não oficial que ajuda a *aplicar* o método; ela não reproduz o livro. Para aprender o PBB na fonte, adquira o livro: <https://leanpub.com/pbb>. A técnica **TAPAs** é de **Manoel Pimentel**. **INVEST** de Bill Wake; **3Cs** de Ron Jeffries; **ARO/FDD** popularizado por Mike Cohn; **Lean Inception** de Paulo Caroli.
