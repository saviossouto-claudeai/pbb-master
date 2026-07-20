# 🗂️ pbb-master

> Uma **Agent Skill** para o [Claude Code](https://claude.com/claude-code) que ajuda a construir, revitalizar e refinar um **Product Backlog** aplicando o método **PBB (Product Backlog Building)** de Fábio Aguiar e Paulo Caroli.
>
> An **Agent Skill** for [Claude Code](https://claude.com/claude-code) that helps you build, revive and refine a **Product Backlog** by applying the **PBB (Product Backlog Building)** method by Fábio Aguiar and Paulo Caroli.

<p align="center"><em>🇧🇷 Português abaixo · 🇺🇸 English below</em></p>

---

## 🇧🇷 Português

### O que é

`pbb-master` é uma skill que transforma o Claude no **facilitador de uma sessão de PBB**. Em vez de você preencher formulários, ele conduz o método passo a passo, conversando, e ao final entrega um backlog pronto em dois formatos: um **PBB Canvas em HTML interativo** e um **export em markdown** pronto pra colar no Jira, Azure DevOps ou Notion.

> ⚠️ Esta skill é uma ferramenta **independente e não oficial** que ajuda a *aplicar* o método. Ela **não reproduz o livro** e usa exemplos originais. Para aprender o PBB na fonte, **compre o livro**: <https://leanpub.com/pbb>.

### O que ela faz — os 3 modos

| Modo | Quando usar | O que acontece |
|---|---|---|
| **1. Construir do zero** | Você tem uma ideia/visão e nenhum backlog | Preenche o PBB Canvas completo (Contexto → Personas → Features → PBIs), prioriza com COORG e gera as User Stories |
| **2. Revitalizar backlog** | Backlog bagunçado, sem ordem, com itens vagos | Diagnostica, mapeia os itens existentes para o canvas, reescreve em ARO, prioriza e corta o que não agrega |
| **3. Quebrar feature grande** | Uma feature/épico grande demais pra uma Sprint | Aplica o **Steps Map** pra fatiar em PBIs pequenos, prioriza e converte em histórias |

### Como ela aplica o método (fiel ao PBB)

- **PBB Canvas** em 4 passos: Contextualize o produto → Descreva as Personas → Entenda as Features (máx. 10) → Identifique os PBIs.
- **Steps Map** (2 etapas) para quebrar cada feature em PBIs pequenos.
- **Modelo ARO** (Ação · Resultado · Objeto) para descrever cada PBI.
- **COORG** (Classificar · Ordenar · ORGanizar) para priorizar o backlog.
- **User Stories** no formato **3Ws** (Como/Posso/Para), com **INVEST**, **3Cs**, **Critérios de Aceite** (Dado/Quando/Então), **Habilitadores** (spike/técnico) e **Tarefas**.
- **TAPAs** (Tangível · Atômica · Preciosa · Acessível) para checar a qualidade das histórias.
- **Definition of Ready / Done** e **refinamento contínuo**.
- Encaixe com a **Lean Inception** (o PBB é o passo seguinte).

### Como usar

1. **Instale a skill** (veja abaixo).
2. Peça algo em linguagem natural — **não precisa dizer "PBB"**:
   - *"me ajuda a montar o backlog do meu app de agendamento"*
   - *"meu backlog no Jira tá uma bagunça, como recupero?"*
   - *"como quebro essa feature de checkout em histórias menores?"*
   - *"já terminei a Lean Inception, e agora?"*
3. O Claude conduz a sessão e entrega o **Canvas HTML** + o **export markdown**.

### Instalação

Como skill pessoal do Claude Code (fica disponível em qualquer projeto):

```bash
git clone https://github.com/<SEU_USUARIO>/pbb-master.git
# copie a pasta para o diretório de skills do Claude Code:
#   macOS/Linux: ~/.claude/skills/pbb-master
#   Windows:     %USERPROFILE%\.claude\skills\pbb-master
```

Depois, numa nova sessão do Claude Code, é só pedir. A skill é reconhecida pela sua descrição — não precisa de comando especial.

### Estrutura

```
pbb-master/
├── SKILL.md            # método, 3 modos, facilitação e formato de saída
├── template.html       # PBB Canvas interativo (HTML autocontido, tema claro/escuro)
├── references/         # detalhamento carregado sob demanda
│   ├── canvas-flow.md      # 4 passos + Steps Map + ARO
│   ├── coorg.md            # Classificar / Ordenar / ORGanizar
│   ├── user-stories.md     # 3Ws, INVEST, 3Cs, Habilitadores, ACs, TAPAs
│   ├── ready-refinement.md # DoR/DoD + refinamento contínuo
│   ├── lean-inception.md   # encaixe pós-Lean Inception
│   └── markdown-export.md  # template do export
└── evals/evals.json    # cenários de teste
```

### Créditos

Método **Product Backlog Building** de **Fábio Aguiar** e **Paulo Caroli** — 📘 <https://leanpub.com/pbb>.
**TAPAs** de Manoel Pimentel · **INVEST** de Bill Wake · **3Cs** de Ron Jeffries · **ARO/FDD** popularizado por Mike Cohn · **Lean Inception** de Paulo Caroli.

---

## 🇺🇸 English

### What it is

`pbb-master` turns Claude into a **PBB session facilitator**. Instead of filling out forms, you let Claude run the method step by step, conversationally, and at the end you get a ready backlog in two formats: an **interactive HTML PBB Canvas** and a **markdown export** ready to paste into Jira, Azure DevOps or Notion.

> ⚠️ This skill is an **independent, unofficial** tool that helps you *apply* the method. It **does not reproduce the book** and uses original examples. To learn PBB from the source, **buy the book**: <https://leanpub.com/pbb>.

### What it does — the 3 modes

| Mode | When | What happens |
|---|---|---|
| **1. Build from scratch** | You have an idea/vision and no backlog | Fills the full PBB Canvas (Context → Personas → Features → PBIs), prioritizes with COORG, generates User Stories |
| **2. Revive a backlog** | Messy, unordered backlog with vague items | Diagnoses, maps existing items onto the canvas, rewrites them in ARO, prioritizes and cuts low value |
| **3. Break a big feature** | A feature/epic too large for a Sprint | Applies the **Steps Map** to slice it into small PBIs, prioritizes and converts into stories |

### How it applies the method (faithful to PBB)

- **PBB Canvas**, 4 steps: Contextualize the product → Describe Personas → Understand Features (max 10) → Identify PBIs.
- **Steps Map** (2 stages) to break each feature into small PBIs.
- **ARO model** (Action · Result · Object) to phrase each PBI.
- **COORG** (Classify · Order · ORGanize) to prioritize the backlog.
- **User Stories** in the **3Ws** format (As/I can/So that), with **INVEST**, **3Cs**, **Acceptance Criteria** (Given/When/Then), **Enablers** (spike/technical) and **Tasks**.
- **TAPAs** (Tangible · Atomic · Precious · Affordable) to check story quality.
- **Definition of Ready / Done** and **continuous refinement**.
- Fits after a **Lean Inception** (PBB is the next step).

### How to use

1. **Install the skill** (see below).
2. Ask in natural language — **you don't need to say "PBB"**:
   - *"help me build the backlog for my scheduling app"*
   - *"my Jira backlog is a mess, how do I fix it?"*
   - *"how do I split this checkout feature into smaller stories?"*
   - *"we just finished a Lean Inception, what now?"*
3. Claude facilitates the session and delivers the **HTML Canvas** + the **markdown export**.

### Installation

As a personal Claude Code skill (available in any project):

```bash
git clone https://github.com/<YOUR_USERNAME>/pbb-master.git
# copy the folder into Claude Code's skills directory:
#   macOS/Linux: ~/.claude/skills/pbb-master
#   Windows:     %USERPROFILE%\.claude\skills\pbb-master
```

Then, in a new Claude Code session, just ask. The skill is picked up from its description — no special command needed.

### Credits

**Product Backlog Building** method by **Fábio Aguiar** and **Paulo Caroli** — 📘 <https://leanpub.com/pbb>.
**TAPAs** by Manoel Pimentel · **INVEST** by Bill Wake · **3Cs** by Ron Jeffries · **ARO/FDD** popularized by Mike Cohn · **Lean Inception** by Paulo Caroli.

---

## 📄 License

The **tooling in this repository** (skill instructions, HTML template, scripts) is released under the [MIT License](LICENSE).
The **PBB method and the book** are the intellectual property of their authors, Fábio Aguiar and Paulo Caroli — this repository does not license or redistribute the book.
