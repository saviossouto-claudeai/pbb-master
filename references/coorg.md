# COORG — a técnica de priorização do PBB

Ao seguir os 4 passos do canvas você chega a uma lista de PBIs = o Backlog. Para times que precisam planejar as próximas entregas/Sprints, aplique mais um passo: o **COORG**.

**COORG = Classificar, Ordenar, ORGanizar.** Ele ajuda a priorizar o backlog para planejar o fluxo de trabalho e/ou as próximas Sprints.

> Exemplos abaixo são **originais**, só ilustrativos. Escolha sempre critérios/escalas do seu próprio contexto.

---

## Etapa 1 — Classificar

Antes de classificar, **defina com o grupo os critérios de classificação e suas escalas**, conforme o contexto do produto. Primeiro alinhe os critérios; só depois pontue os PBIs.

### Exemplo (original, ilustrativo)

Dois critérios possíveis:
- **Frequência de uso** — com que frequência o usuário aciona o PBI (cada PBI é um passo do fluxo de uma feature).
- **Valor de negócio** — o valor gerado quando o usuário aciona o PBI.

Uma escala possível para "frequência de uso":

| Escala | Pontos |
|---|---|
| várias vezes ao dia | 5 |
| uma vez ao dia | 4 |
| algumas vezes na semana | 3 |
| mensal | 2 |
| raramente | 1 |

Uma escala possível para "valor de negócio":

| Escala | Pontos |
|---|---|
| Alto | 3 |
| Médio | 2 |
| Baixo | 1 |

### A fórmula

Defina uma fórmula que combine os critérios. Ex. (ilustrativo): **Prioridade = Frequência de uso + Valor de negócio**. Note que dois PBIs podem empatar por caminhos diferentes (5+1 e 3+3 dão 6).

**DICA:** Decida critérios, escalas e fórmula que façam sentido no **seu** contexto — não existe fórmula única. Classifique cada PBI e anote o resultado. Quanto maior a pontuação, maior a prioridade.

---

## Etapa 2 — Ordenar

Ordene as **features** numa sequência lógica, da **esquerda para a direita**, estruturando-as como uma narrativa que faça sentido para o time e o contexto. Ao mover uma feature, mova junto seus PBIs (abaixo dela).

- Um time pode ordenar as features segundo uma **user journey**.
- Um time que veio de uma **Lean Inception** segue a ordem do **Sequenciador** (a ordem em que decidiram trabalhar nas features) — nesse caso a etapa Ordenar já está feita.

---

## Etapa 3 — ORGanizar

Para cada feature, organize os PBIs **de cima para baixo por prioridade**: a maior pontuação na primeira linha, a próxima abaixo, e assim por diante.

O COORG organiza os PBIs numa **matriz** (features nas colunas, prioridade decrescente nas linhas). Para converter em uma **lista ordenada de trabalho**, percorra a matriz **da esquerda para a direita, de cima para baixo**: primeiro a linha de topo inteira (esquerda→direita), depois a segunda linha, e assim até o fim.

**Diga "NÃO".** Geralmente os itens com nota baixa **não entram** no backlog — o COORG deixa claro o valor reduzido deles no contexto. É o momento em que o Product Owner usa seu poder de decisão para recusar itens de baixa classificação.

> Resultado: **backlog inicial alinhado e priorizado.**

---

## Atualize o backlog para novos PBIs

O resultado do COORG **não é definitivo** — é uma priorização inicial que evolui com o backlog.

- Itens que surgem durante uma Sprint **não interrompem** a Sprint (a Sprint é intocável), mas precisam ser adaptados e priorizados no backlog.
- No momento adequado, **reaplique o COORG**: Classifique os novos → Ordene conforme a feature → re-Organize o backlog inteiro segundo a pontuação de todos (novos + antigos).

Para transformar feedback/insights em novos PBIs ou features antes de reaplicar o COORG, ver `ready-refinement.md`.
