# O fluxo de construção do Backlog — PBB Canvas

O PBB Canvas oferece um fluxo simples que ajuda a entender a necessidade do cliente e construir o backlog. São 4 passos, nesta ordem:

1. Contextualize o Produto
2. Descreva as Personas
3. Entenda as Features
4. Identifique os PBIs

Facilite um bloco por vez. As perguntas em **negrito** conduzem cada bloco.

> Os exemplos abaixo são **originais**, apenas ilustrativos. O método é do livro PBB (Aguiar & Caroli); os exemplos foram criados para esta skill.

---

## Passo 1 — Contextualize o produto

Esclareça o que é o produto, os problemas/dores e as expectativas. Três blocos:

### PRODUCT NAME
Identifique o produto que será construído.
> Provoque: **"Se esse produto estivesse numa caixa na prateleira, que nome estaria na caixa?"**

### PROBLEMS (estado atual)
Compreenda o estado atual listando os problemas e dores do contexto.
> **"Quais são os principais problemas e dores de hoje?"**

**DICA:** Descreva os problemas de forma **macro**. Detalhes a nível de features vêm mais adiante.

### EXPECTATIONS (estado desejado)
Liste as expectativas para o futuro do produto — o que ajuda a resolver os problemas do estado atual.
> **"O que se espera do produto? Onde queremos chegar?"**

**DICA:** Liste só as expectativas. Evite descrever a solução em detalhe.

> **Entenda o problema antes da solução.** Aguiar e Caroli resumem isso numa analogia: aja como o médico que investiga a queixa antes de receitar, não como o garçom que só anota o pedido. Levante os problemas antes de saltar para soluções. Em cenário incerto, itens de backlog são **hipóteses** a validar, não requisitos fechados. Problemas e expectativas se relacionam em muitos-para-muitos e formam o pano de fundo do resto do PBB.

> Se o time vem de uma Lean Inception, estes blocos podem ser preenchidos a partir dos artefatos dela ou deixados vazios. Ver `lean-inception.md`.

---

## Passo 2 — Descreva as Personas

Uma persona representa um usuário do produto: papel + necessidades + dores. Cria uma representação realística de quem vai usar o produto.

> **"Qual o perfil da persona? O que ela faz? O que ela espera?"**

- **Perfil** → vai compor o "quem" da história de usuário depois.
- **O que faz** → descreva como **atividade**, geralmente o que a persona faz hoje. Ex. (original): *(Gestora de RH) (fecha a folha de ponto no fim do mês)*.
- **O que espera** → algo que a persona deseja do produto. Ex.: *(Gestora de RH) (aprovar horas extras sem planilha)*.

Aproveite qualquer trabalho prévio (mapa de empatia, discovery, inception). No PBB, o foco é **perfil + atividades**, insumo do passo seguinte.

---

## Passo 3 — Entenda as Features

Feature = a descrição de uma **ação ou interação de uma persona com o produto**. A descrição deve ser a mais simples possível. Ex. (originais): agendar uma consulta, exportar um relatório, aprovar uma despesa.

Releia cada atividade das personas buscando ações/interações com o produto. Cada uma vira uma Feature.

> **"O usuário quer fazer algo; o produto precisa de uma feature para isso. Qual é? Que problemas da persona ela resolve? Que benefícios ela traz?"**

**DICA:** Anote os **Problemas** em post-its à **esquerda** e os **Benefícios** à **direita** da descrição da feature.

**Exemplo original:** persona *(Gestora de RH)* com atividade *(aprovar horas extras)* → feature **(aprovar despesa/hora extra)**.
- Problemas: *(aprovação por e-mail se perde)*, *(sem trilha de quem aprovou o quê)*.
- Benefícios: *(aprovação rastreável)*, *(menos retrabalho no fechamento)*.

**DICA CRÍTICA:** Limite o total a **no máximo 10 features**. Mais que isso vira inventário, não backlog. Se surgirem muitas, priorize e selecione as mais importantes.

> **Features vs. User Stories:** features estão num nível mais alto que histórias. No canvas, primeiro **identificamos, entendemos e priorizamos features**; só depois as detalhamos em User Stories.

---

## Passo 4 — Identifique os PBIs (via Steps Map)

PBIs (Product Backlog Items) são os elementos que compõem o Product Backlog. Para cada feature, quebre-a em PBIs menores e mais precisos usando o **Steps Map**.

> **"Qual o primeiro item de trabalho (passo) desta feature? E o segundo? E os próximos?"**

**DICA:** Organize os itens **verticalmente** — o que está mais acima tem maior prioridade (a prioridade é a próxima etapa).

### Steps Map — a técnica de quebra

O Steps Map quebra uma feature em pequenos passos; **cada passo será um PBI**. Aplica-se em **duas etapas**:

**Etapa 1 — Defina o passo a passo do fluxo de trabalho.**
Pergunte o primeiro item de trabalho da feature e anote. Depois o segundo, o terceiro, e assim por diante. Cada item é um passo para construir a feature.

> Exemplo original — feature **[Aprovar despesa]**:
> [Listar as despesas pendentes] → [Abrir o detalhe de uma despesa] → [Registrar a decisão de aprovação] → [Notificar o solicitante] → …

**Etapa 2 — Evolua cada passo com perguntas, comentários e ideias.**
Para cada passo, peça que todos escrevam, individualmente, um post-it por questionamento/comentário/ideia. Sugestão de cores: **laranja = questionamentos, verde = comentários, azul = ideias.**

> Um **questionamento** pode eliminar um passo desnecessário; um **comentário** pode melhorar um passo útil; uma **ideia** pode fazer nascer um passo novo.

Fazer individualmente por escrito evita que alguém de maior influência domine as decisões. Se o grupo colabora bem, pode ser verbal. Ao final, **cada passo do fluxo é um PBI**.

**Depois do Steps Map, cheque cada PBI com o teste da fatia** (`fatiamento.md`, técnica complementar ao PBB). Um passo como "Listar as despesas pendentes" pode não servir a ninguém sozinho: junte-o ao passo vizinho ou refaça o corte para que alguém consiga usá-lo. Um passo grande demais para o SLE do time é fatiado com os padrões de lá.

> **Steps Map ≠ User Journey.** A User Journey descreve o caminho do usuário até um objetivo. O Steps Map descreve o **fluxo de trabalho** — o que precisa ser construído para completar a feature. Coincidem quando ambos refletem, na mesma ordem, o que o usuário faz e o que precisa ser feito.

### Descreva a ação de cada PBI — modelo ARO

Cada PBI representa uma ação de um usuário no produto e deve ser descrito no **modelo ARO** (originado da metodologia FDD; formato popularizado por Mike Cohn):

> **ARO = Ação + Resultado + Objeto**
> Comece pela **Ação** (verbo), depois o **Resultado**, e termine com o **Objeto** no contexto.
> Formato: **[Ação] [Resultado] por | para | de | em [Objeto]**.

Exemplos (originais):
- Registrar a decisão de aprovação da despesa.
- Exportar o relatório de horas do mês.
- Calcular o total de reembolsos por centro de custo.
- Gerar o comprovante de aprovação.

**Corrigindo um PBI mal escrito:** "Despesa aprovada" não é ARO — *aprovada* já é o resultado, sem uma ação clara. Reescreva com um verbo de ação: **Registrar** (ação) **a aprovação** (resultado) **da despesa** (objeto).

Ao final do passo 4 você tem a lista de PBIs = o Backlog. Para muitos times isso basta; quem planeja Sprints segue para o **COORG** (`coorg.md`). Depois, cada PBI vira uma User Story (`user-stories.md`).
