---
name: pbb-master
description: Use para construir, revitalizar ou refinar um Product Backlog com o método PBB (Fábio Aguiar e Paulo Caroli), no processo completo (PBB Canvas em HTML + export markdown) ou em uso pontual do dia a dia, aplicando só uma prática, com resposta pronta para colar no Jira/Azure DevOps. Acione mesmo sem a sigla "PBB" quando alguém quiser criar backlog do zero, organizar um backlog bagunçado, quebrar feature/épico em PBIs, fatiar uma história grande em itens menores que ainda entreguem valor, escrever user stories (3Ws) ou critérios de aceite, revisar se uma história está boa (INVEST/TAPAs) ou ready (DoR), reescrever itens em ARO, priorizar itens (COORG), transformar feedback em PBI, preparar refinamento ou seguir após uma Lean Inception. Exemplos — "fatia essa história", "escreve os critérios de aceite", "esse item tá ready?", "prioriza esses 6 itens". Also for building, refining or splitting backlogs and user stories in English.
---

# PBB Master — Product Backlog Building

## O que é

PBB (Product Backlog Building) é o método de Fábio Aguiar e Paulo Caroli para **construir colaborativamente um Product Backlog efetivo**. Ele complementa o Scrum: o Scrum define o backlog como artefato central mas não diz como construí-lo — o PBB preenche essa lacuna com um canvas visual e um fluxo simples.

Esta skill **aplica o método**; ela não substitui o livro. Os exemplos nos arquivos de referência são **originais**. Para aprender o método na fonte, compre o livro (ver Créditos no fim).

**Princípio-guia: entenda o problema antes da solução.** Os autores resumem isso numa analogia (aja como o médico que investiga a queixa antes de receitar, não como o garçom que só anota o pedido). Ao construir backlog, levante os **problemas** antes de saltar para soluções. Em cenário complexo, backlog é uma lista de **hipóteses** a validar, não de requisitos fechados.

**Simples, rápido e enxuto.** Uma sessão de PBB dura de 2 a 8 horas e gera backlog suficiente para as **próximas 2 a 5 Sprints** — não um inventário completo. Linguagem acessível: qualquer interessado consegue participar. Não adicione passos ao fluxo do canvas. A única técnica de fora do método é o **fatiamento vertical** (`references/fatiamento.md`), usado só para quebrar PBIs e histórias grandes demais; quando usá-lo, diga que é complementar ao PBB.

Quando o usuário pedir algo fora do PBB, diga o que o PBB oferece e ofereça a alternativa mais próxima do método.

**Quem costuma usar esta skill** é o Agile Master, o Scrum Master ou o próprio PO, no apoio ao backlog. Ao apoiar o PO: proponha opções, mostre o porquê, faça as perguntas certas, e deixe **valor e ordem com o PO**. Não decida a prioridade por ele.

## Os modos de uso

Identifique o modo pelo pedido (pode ser mais de um em sequência). **Na dúvida, prefira o uso pontual** e ofereça o processo completo em uma linha: quem pede uma coisa quer essa coisa, não uma sessão.

| Modo | Quando | Fluxo |
|---|---|---|
| **0. Uso pontual (dia a dia)** | Pedido sobre um item ou uma prática: "fatia essa história", "escreve os critérios de aceite", "esse item tá ready?", "reescreve em ARO", "prioriza esses 6 itens", "chegou esse feedback, onde encaixa?" | Só a prática pedida → resposta direta, pronta para colar (ver seção abaixo) |
| **1. Construir backlog do zero** | "quero criar o backlog do produto X", "tenho uma ideia/visão e preciso de backlog", "saímos de uma Lean Inception/discovery" | Preencher o PBB Canvas completo (4 passos) → COORG → gerar User Stories |
| **2. Revitalizar backlog bagunçado** | "meu backlog é uma bagunça", "tenho 200 itens sem ordem", "backlog abandonado/mal gerido" | Diagnóstico → mapear itens existentes para o Canvas → COORG → cortar o que não agrega → refinamento contínuo |
| **3. Quebrar feature grande** | "essa funcionalidade é enorme", "como divido esse épico?" | Steps Map na feature → PBIs em ARO → **teste da fatia** em cada PBI (fatiar ou juntar os que falharem) → COORG → User Stories + habilitadores |

Nos modos 1 a 3, **comece entendendo o contexto conversando** — não peça para o usuário preencher um formulário gigante. Faça as perguntas do passo em que ele está, uma seção por vez, como uma facilitadora faria. Você é a **facilitadora do PBB**.

## Uso pontual (modo 0)

Aplique **só** a prática pedida. Não abra o canvas, não faça a sessão completa, não gere HTML.

| Pedido | Prática | Leia | Entregue |
|---|---|---|---|
| "Essa história/PBI tá grande", "fatia", "quebra em itens menores" | Fatiamento vertical (complementar) | `fatiamento.md` | 2–3 formas de cortar; fatias como histórias com ACs; teste da fatia de cada uma; sugestão da primeira fatia |
| "Quebra essa feature/épico em PBIs" | Steps Map + teste da fatia | `canvas-flow.md` (passo 4), `fatiamento.md` | PBIs em ARO na ordem do fluxo, marcando os que não passam no teste da fatia |
| "Reescreve em ARO", "esse PBI tá mal escrito" | Modelo ARO | `canvas-flow.md` (passo 4) | Antes → depois, com o motivo em uma linha |
| "Escreve a história", "escreve os critérios de aceite" | 3Ws + Dado/Quando/Então | `user-stories.md` | História + ACs; se passar de 5 ACs, avise e sugira fatiar |
| "Essa história tá boa?", "revisa essas histórias" | INVEST + TAPAs | `user-stories.md` | Tabela com veredito por atributo, o problema e a correção sugerida |
| "Esse item tá ready?", "pode entrar na Sprint?" | Definition of Ready | `ready-refinement.md` | Checklist do DoR com lacunas e as perguntas para o PO fechar cada uma. Use o DoR do time; sem um, use o exemplo de `ready-refinement.md` e diga isso |
| "Prioriza esses itens" | COORG | `coorg.md` | Critérios e escalas (pergunte ou proponha para o PO validar), tabela pontuada e lista ordenada |
| "Chegou esse feedback/pedido, onde encaixa?" | Estruturar feedback | `ready-refinement.md` | PBI ou feature, a qual persona/feature se liga, e o item já em ARO |
| "Isso é história ou é técnico?", "precisa de spike?" | Habilitadores | `user-stories.md` | Habilitador em ARO e quais histórias ele habilita |
| "Prepara o refinamento", "pauta do refinamento" | Refinamento contínuo | `ready-refinement.md`, `fatiamento.md` | Itens das próximas 1–3 Sprints, o que falta em cada um (DoR) e perguntas de fatiamento para levar ao time |

Regras do uso pontual:
- **Trabalhe com o que o usuário trouxe.** Persona e valor (o "Para…") são necessários para história e fatiamento: se faltarem, pergunte uma vez. Se o usuário não estiver para responder, proponha e marque como **hipótese para o PO validar**.
- **Saída em markdown**, curta, pronta para colar no Jira/Azure DevOps/Notion (modelos curtos em `markdown-export.md`). Sem canvas HTML, a menos que peçam.
- Se o item revelar um problema maior (ninguém sabe a persona, a feature não está clara, o backlog inteiro tem o mesmo defeito), diga em uma linha e ofereça o modo completo correspondente.
- Termine com no máximo **uma** sugestão de próximo passo, ligada ao que apareceu (ex.: "a fatia 4 depende de um spike; quer que eu escreva?").

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
- **`references/fatiamento.md`** — técnica **complementar**: teste da fatia (utilizável, valor, vertical, testável, cabe no SLE), padrões de corte (SPIDR e outros), anti-padrões. Leia sempre que for quebrar um PBI/história, ou depois do Steps Map para checar os PBIs.

Regra prática: **não recite as referências de cor**. Abra o arquivo, siga a técnica exatamente como está escrita, use os exemplos como modelo (mas adapte ao contexto real do usuário).

## Como conduzir uma sessão (facilitação, modos 1 a 3)

1. **Descubra o modo e o ponto de partida.** Pergunte o que já existe (visão, discovery, Lean Inception, backlog atual, uma feature específica).
2. **Facilite passo a passo.** Faça as perguntas de cada bloco do canvas, uma de cada vez. Reflita de volta o que entendeu antes de avançar. Provoque a colaboração — no PBB, um questionamento pode eliminar um passo, um comentário pode melhorar um passo e uma ideia pode criar um passo novo.
3. **Mantenha enxuto.** Limite features a 10. Não refine itens que só serão feitos muitas Sprints à frente (refine só as próximas 1–3 Sprints). Planeje uma trilha ajustável, não um trilho fixo.
4. **Priorize com COORG** quando o usuário precisar planejar Sprints/ordem de entrega.
5. **Gere os entregáveis** (canvas + user stories) e **produza a saída** (ver abaixo).

## Produzindo a saída

**Uso pontual (modo 0):** só markdown na resposta, nos modelos curtos de `references/markdown-export.md`. Não gere canvas.

**Modos 1 a 3:** o usuário quer **dois entregáveis**: um **PBB Canvas em HTML interativo** e um **export em markdown**.

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
- Fatiar **não é quebrar em tarefas**: front, API e banco são tarefas do time, não itens de backlog. Cada fatia precisa ser utilizável e ter valor próprio (`fatiamento.md`).
- Para checar tamanho, use o **SLE do time** (right-sizing), não story points: "provavelmente termina dentro do nosso SLE?".

Se o usuário pedir algo assim, explique a distinção do método e ofereça o caminho PBB correto.

## Créditos

Método **Product Backlog Building** de **Fábio Aguiar** e **Paulo Caroli**. Esta skill é uma ferramenta independente e não oficial que ajuda a *aplicar* o método; ela não reproduz o livro. Para aprender o PBB na fonte, adquira o livro: <https://leanpub.com/pbb>. A técnica **TAPAs** é de **Manoel Pimentel**. **INVEST** de Bill Wake; **3Cs** de Ron Jeffries; **ARO/FDD** popularizado por Mike Cohn; **Lean Inception** de Paulo Caroli. Técnicas complementares de fatiamento: **SPIDR** de Mike Cohn; padrões de divisão de histórias de **Richard Lawrence**; **Hamburger Method** de Gojko Adzic; **Elephant Carpaccio** de Alistair Cockburn; *right-sizing* pelo SLE de **Daniel Vacanti**.
