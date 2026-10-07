# 🗂️ pbb-master

> Uma **Agent Skill** para o [Claude](https://claude.ai) e o [Claude Code](https://claude.com/claude-code) que ajuda a construir, revitalizar e refinar um **Product Backlog** aplicando o método **PBB (Product Backlog Building)** de Fábio Aguiar e Paulo Caroli — na sessão completa ou no dia a dia, uma prática de cada vez.
>
> An **Agent Skill** for [Claude](https://claude.ai) and [Claude Code](https://claude.com/claude-code) that helps you build, revive and refine a **Product Backlog** by applying the **PBB (Product Backlog Building)** method by Fábio Aguiar and Paulo Caroli — as a full session or day to day, one practice at a time.

<p align="center"><em>🇧🇷 Português abaixo · 🇺🇸 English below</em></p>

---

## 🇧🇷 Português

### O que é

`pbb-master` transforma o Claude no **facilitador do PBB** e num **parceiro de refinamento** para quem apoia o backlog no dia a dia (PO, Agile Master, Scrum Master). Ela funciona de dois jeitos:

- **Sessão completa:** conduz o método passo a passo, conversando, e entrega o backlog em dois formatos: um **PBB Canvas em HTML interativo** e um **export em markdown** pronto para colar no Jira, Azure DevOps ou Notion.
- **Uso pontual:** aplica **só a prática que você pediu** (fatiar uma história, escrever critérios de aceite, checar se o item está ready, priorizar alguns itens…) e devolve o resultado direto, em markdown, sem canvas.

> ⚠️ Esta skill é uma ferramenta **independente e não oficial** que ajuda a *aplicar* o método. Ela **não reproduz o livro** e usa exemplos originais. Para aprender o PBB na fonte, **compre o livro**: <https://leanpub.com/pbb>.

### O que ela faz — os modos

| Modo | Quando usar | O que acontece |
|---|---|---|
| **0. Uso pontual (dia a dia)** | Você precisa de uma prática só, sobre um item ou alguns itens | Aplica só aquela prática e devolve markdown pronto para colar, sem canvas |
| **1. Construir do zero** | Você tem uma ideia/visão e nenhum backlog | Preenche o PBB Canvas completo (Contexto → Personas → Features → PBIs), prioriza com COORG e gera as User Stories |
| **2. Revitalizar backlog** | Backlog bagunçado, sem ordem, com itens vagos | Diagnostica, mapeia os itens existentes para o canvas, reescreve em ARO, prioriza e corta o que não agrega |
| **3. Quebrar feature grande** | Uma feature/épico grande demais para uma Sprint | Aplica o **Steps Map** para quebrar em PBIs, checa cada um com o **teste da fatia**, prioriza e converte em histórias |

Na dúvida, a skill escolhe o uso pontual e oferece a sessão completa em uma linha.

### Uso pontual — o que você pode pedir

| Você pede | Você recebe |
|---|---|
| "Fatia essa história" / "quebra em itens menores" | 2 ou 3 formas de cortar, as fatias como histórias com critérios de aceite, o teste da fatia de cada uma e a sugestão da primeira fatia |
| "Quebra essa feature em PBIs" | Steps Map com os PBIs em ARO, marcando os que não passam no teste da fatia |
| "Reescreve em ARO" | Antes → depois, com o motivo |
| "Escreve a história" / "escreve os critérios de aceite" | História em 3Ws e critérios em Dado/Quando/Então |
| "Essa história tá boa?" | Revisão por INVEST e TAPAs, com a correção sugerida |
| "Esse item tá ready?" | As lacunas do DoR e as perguntas para o PO fechar cada uma |
| "Prioriza esses itens" | COORG só naqueles itens, com critérios para o PO validar |
| "Chegou esse feedback, onde encaixa?" | Se é PBI ou feature, a que persona/feature se liga, já em ARO |
| "Isso é história ou é técnico?" | Habilitador (spike ou técnico) em ARO e quais histórias ele habilita |
| "Prepara o refinamento" | Itens das próximas 1–3 Sprints, o que falta em cada um e perguntas de fatiamento |

A skill **propõe**, mas **valor e ordem ficam com o PO**: ela apresenta opções e o porquê, não decide a prioridade por ele.

### O teste da fatia

Fatiar não é quebrar em tarefas: "fazer o front", "fazer a API" e "criar o banco" não servem a ninguém sozinhos. Cada pedaço precisa passar em cinco perguntas:

1. **Utilizável:** se só esta fatia ficar pronta, alguém consegue usar ou ver o resultado?
2. **Valor validável:** o PO consegue demonstrar e aprender algo com ela?
3. **Vertical:** atravessa as camadas necessárias para funcionar?
4. **Testável:** tem critérios de aceite próprios, no máximo 5?
5. **Cabe no SLE:** o time acredita que termina dentro do seu SLE (ex.: "85% dos itens em até 8 dias")?

A pergunta 5 é o *right-sizing* de Daniel Vacanti: checa o tamanho sem story points, coerente com o PBB, que não estima esforço. Para cortar, a skill usa padrões consagrados (SPIDR, padrões de Richard Lawrence, Hamburger) e diz explicitamente que essa técnica é **complementar** ao PBB.

### Como ela aplica o método (fiel ao PBB)

- **PBB Canvas** em 4 passos: Contextualize o produto → Descreva as Personas → Entenda as Features (máx. 10) → Identifique os PBIs.
- **Steps Map** (2 etapas) para quebrar cada feature em PBIs.
- **Modelo ARO** (Ação · Resultado · Objeto) para descrever cada PBI.
- **COORG** (Classificar · Ordenar · ORGanizar) para priorizar o backlog.
- **User Stories** no formato **3Ws** (Como/Posso/Para), com **INVEST**, **3Cs**, **Critérios de Aceite** (Dado/Quando/Então), **Habilitadores** (spike/técnico) e **Tarefas**.
- **TAPAs** (Tangível · Atômica · Preciosa · Acessível) para checar a qualidade das histórias.
- **Definition of Ready / Done** e **refinamento contínuo**.
- Encaixe com a **Lean Inception** (o PBB é o passo seguinte).
- **Complementar ao método:** fatiamento vertical com o teste da fatia (seção acima). O fluxo do canvas continua exatamente o do livro.

### Como usar

1. **Instale a skill** (veja abaixo).
2. Peça em linguagem natural — **não precisa dizer "PBB"**.

   Sessão completa:
   - *"me ajuda a montar o backlog do meu app de agendamento"*
   - *"meu backlog no Jira tá uma bagunça, como recupero?"*
   - *"já terminei a Lean Inception, e agora?"*

   Dia a dia:
   - *"fatia essa história: Como gestor, posso gerenciar as férias da equipe, para planejar a capacidade"*
   - *"escreve os critérios de aceite dessa história pra eu colar no Azure"*
   - *"esse item pode entrar na sprint? 'Melhorar a tela de relatórios'"*
   - *"prioriza esses 5 itens pra mim"*
3. Na sessão completa, o Claude conduz e entrega o **Canvas HTML** + o **export markdown**. No uso pontual, responde direto com o markdown da prática pedida.

### Instalação

**No Claude (app e web):** baixe este repositório como `.zip` (botão **Code → Download ZIP**), garanta que a pasta compactada se chama `pbb-master` e envie-a como skill nas configurações do Claude.

**No Claude Code** (skill pessoal, disponível em qualquer projeto):

```bash
git clone https://github.com/saviossouto-claudeai/pbb-master.git
# copie a pasta para o diretório de skills do Claude Code:
#   macOS/Linux: ~/.claude/skills/pbb-master
#   Windows:     %USERPROFILE%\.claude\skills\pbb-master
```

Depois, numa nova conversa ou sessão, é só pedir. A skill é reconhecida pela descrição — não precisa de comando especial.

### Estrutura

```
pbb-master/
├── SKILL.md            # método, modos (incl. uso pontual), facilitação e formato de saída
├── template.html       # PBB Canvas interativo (HTML autocontido, tema claro/escuro)
├── references/         # detalhamento carregado sob demanda
│   ├── canvas-flow.md      # 4 passos + Steps Map + ARO
│   ├── coorg.md            # Classificar / Ordenar / ORGanizar
│   ├── user-stories.md     # 3Ws, INVEST, 3Cs, Habilitadores, ACs, TAPAs
│   ├── ready-refinement.md # DoR/DoD + refinamento contínuo
│   ├── lean-inception.md   # encaixe pós-Lean Inception
│   ├── fatiamento.md       # fatiamento vertical + teste da fatia (complementar)
│   └── markdown-export.md  # template do export + modelos curtos do uso pontual
└── evals/evals.json    # cenários de teste (sessão completa e uso pontual)
```

### Novidades

**Outubro de 2026**
- **Uso pontual (modo 0):** cada prática pode ser usada sozinha, com resposta pronta para colar, sem abrir o canvas.
- **Fatiamento vertical** (`references/fatiamento.md`): teste da fatia, padrões de corte, anti-padrões e exemplo completo.
- O **Steps Map** agora termina com o teste da fatia em cada PBI.
- Novos cenários de teste para o uso pontual.

### Créditos

Método **Product Backlog Building** de **Fábio Aguiar** e **Paulo Caroli** — 📘 <https://leanpub.com/pbb>.
**TAPAs** de Manoel Pimentel · **INVEST** de Bill Wake · **3Cs** de Ron Jeffries · **ARO/FDD** popularizado por Mike Cohn · **Lean Inception** de Paulo Caroli.
Técnicas complementares de fatiamento: **SPIDR** de Mike Cohn · padrões de divisão de histórias de **Richard Lawrence** · **Hamburger Method** de Gojko Adzic · **Elephant Carpaccio** de Alistair Cockburn · *right-sizing* pelo SLE de **Daniel Vacanti**.

---

## 🇺🇸 English

### What it is

`pbb-master` turns Claude into a **PBB facilitator** and a **refinement partner** for whoever supports the backlog day to day (PO, Agile Master, Scrum Master). It works in two ways:

- **Full session:** runs the method step by step, conversationally, and delivers the backlog in two formats: an **interactive HTML PBB Canvas** and a **markdown export** ready to paste into Jira, Azure DevOps or Notion.
- **Day-to-day use:** applies **only the practice you asked for** (split a story, write acceptance criteria, check whether an item is ready, prioritize a few items…) and returns the result directly, in markdown, with no canvas.

> ⚠️ This skill is an **independent, unofficial** tool that helps you *apply* the method. It **does not reproduce the book** and uses original examples. To learn PBB from the source, **buy the book**: <https://leanpub.com/pbb>.

### What it does — the modes

| Mode | When | What happens |
|---|---|---|
| **0. Day-to-day use** | You need a single practice, on one item or a few | Applies only that practice and returns paste-ready markdown, no canvas |
| **1. Build from scratch** | You have an idea/vision and no backlog | Fills the full PBB Canvas (Context → Personas → Features → PBIs), prioritizes with COORG, generates User Stories |
| **2. Revive a backlog** | Messy, unordered backlog with vague items | Diagnoses, maps existing items onto the canvas, rewrites them in ARO, prioritizes and cuts low value |
| **3. Break a big feature** | A feature/epic too large for a Sprint | Applies the **Steps Map** to break it into PBIs, checks each one with the **slice test**, prioritizes and converts into stories |

When in doubt, the skill picks day-to-day use and offers the full session in one line.

### Day-to-day use — what you can ask

| You ask | You get |
|---|---|
| "Split this story" / "break it into smaller items" | 2 or 3 ways to cut, the slices as stories with acceptance criteria, the slice test for each and a suggested first slice |
| "Break this feature into PBIs" | Steps Map with PBIs in ARO, flagging those that fail the slice test |
| "Rewrite this in ARO" | Before → after, with the reason |
| "Write the story" / "write the acceptance criteria" | Story in 3Ws and criteria in Given/When/Then |
| "Is this story any good?" | INVEST and TAPAs review, with the suggested fix |
| "Is this item ready?" | The DoR gaps and the questions the PO needs to answer to close each one |
| "Prioritize these items" | COORG on just those items, with criteria for the PO to validate |
| "We got this feedback, where does it fit?" | Whether it is a PBI or a feature, which persona/feature it belongs to, already in ARO |
| "Is this a story or technical work?" | An enabler (spike or technical) in ARO and which stories it enables |
| "Prepare the refinement" | Items for the next 1–3 Sprints, what each one is missing and slicing questions |

The skill **proposes**, but **value and order stay with the PO**: it lays out options and the reasoning, it does not decide priority for them.

### The slice test

Slicing is not splitting into tasks: "build the front end", "build the API" and "create the database" are useless to anyone on their own. Each piece has to pass five questions:

1. **Usable:** if only this slice is done, can someone use it or see the result?
2. **Verifiable value:** can the PO demonstrate it and learn something from it?
3. **Vertical:** does it cut through the layers it needs to work?
4. **Testable:** does it have its own acceptance criteria, five at most?
5. **Fits the SLE:** does the team believe it will finish within its SLE (e.g. "85% of items within 8 days")?

Question 5 is Daniel Vacanti's *right-sizing*: it checks size without story points, consistent with PBB, which does not estimate effort. To cut, the skill uses well-known patterns (SPIDR, Richard Lawrence's patterns, Hamburger) and says explicitly that this technique is **complementary** to PBB.

### How it applies the method (faithful to PBB)

- **PBB Canvas**, 4 steps: Contextualize the product → Describe Personas → Understand Features (max 10) → Identify PBIs.
- **Steps Map** (2 stages) to break each feature into PBIs.
- **ARO model** (Action · Result · Object) to phrase each PBI.
- **COORG** (Classify · Order · ORGanize) to prioritize the backlog.
- **User Stories** in the **3Ws** format (As/I can/So that), with **INVEST**, **3Cs**, **Acceptance Criteria** (Given/When/Then), **Enablers** (spike/technical) and **Tasks**.
- **TAPAs** (Tangible · Atomic · Precious · Affordable) to check story quality.
- **Definition of Ready / Done** and **continuous refinement**.
- Fits after a **Lean Inception** (PBB is the next step).
- **Complementary to the method:** vertical slicing with the slice test (section above). The canvas flow stays exactly as in the book.

### How to use

1. **Install the skill** (see below).
2. Ask in natural language — **you don't need to say "PBB"**.

   Full session:
   - *"help me build the backlog for my scheduling app"*
   - *"my Jira backlog is a mess, how do I fix it?"*
   - *"we just finished a Lean Inception, what now?"*

   Day to day:
   - *"split this story: As a manager, I can manage my team's vacations, so that I can plan capacity"*
   - *"write the acceptance criteria for this story so I can paste them into Azure"*
   - *"can this item go into the sprint? 'Improve the reports screen'"*
   - *"prioritize these 5 items for me"*
3. In a full session, Claude facilitates and delivers the **HTML Canvas** + the **markdown export**. In day-to-day use, it answers directly with the markdown for the practice you asked for.

> The skill instructions are written in Portuguese, but Claude answers in the language you use.

### Installation

**In Claude (app and web):** download this repository as a `.zip` (**Code → Download ZIP**), make sure the zipped folder is named `pbb-master`, and upload it as a skill in Claude's settings.

**In Claude Code** (personal skill, available in any project):

```bash
git clone https://github.com/saviossouto-claudeai/pbb-master.git
# copy the folder into Claude Code's skills directory:
#   macOS/Linux: ~/.claude/skills/pbb-master
#   Windows:     %USERPROFILE%\.claude\skills\pbb-master
```

Then, in a new conversation or session, just ask. The skill is picked up from its description — no special command needed.

### Structure

```
pbb-master/
├── SKILL.md            # method, modes (incl. day-to-day use), facilitation and output format
├── template.html       # interactive PBB Canvas (self-contained HTML, light/dark theme)
├── references/         # detail loaded on demand
│   ├── canvas-flow.md      # 4 steps + Steps Map + ARO
│   ├── coorg.md            # Classify / Order / ORGanize
│   ├── user-stories.md     # 3Ws, INVEST, 3Cs, Enablers, ACs, TAPAs
│   ├── ready-refinement.md # DoR/DoD + continuous refinement
│   ├── lean-inception.md   # fitting PBB after a Lean Inception
│   ├── fatiamento.md       # vertical slicing + slice test (complementary)
│   └── markdown-export.md  # export template + short day-to-day templates
└── evals/evals.json    # test scenarios (full session and day-to-day use)
```

### What's new

**October 2026**
- **Day-to-day use (mode 0):** each practice can be used on its own, with paste-ready output and no canvas.
- **Vertical slicing** (`references/fatiamento.md`): slice test, cutting patterns, anti-patterns and a full example.
- The **Steps Map** now ends with the slice test on each PBI.
- New test scenarios for day-to-day use.

### Credits

**Product Backlog Building** method by **Fábio Aguiar** and **Paulo Caroli** — 📘 <https://leanpub.com/pbb>.
**TAPAs** by Manoel Pimentel · **INVEST** by Bill Wake · **3Cs** by Ron Jeffries · **ARO/FDD** popularized by Mike Cohn · **Lean Inception** by Paulo Caroli.
Complementary slicing techniques: **SPIDR** by Mike Cohn · story splitting patterns by **Richard Lawrence** · **Hamburger Method** by Gojko Adzic · **Elephant Carpaccio** by Alistair Cockburn · SLE-based *right-sizing* by **Daniel Vacanti**.

---

## 📄 License

The **tooling in this repository** (skill instructions, HTML template, scripts) is released under the [MIT License](LICENSE).
The **PBB method and the book** are the intellectual property of their authors, Fábio Aguiar and Paulo Caroli — this repository does not license or redistribute the book.
