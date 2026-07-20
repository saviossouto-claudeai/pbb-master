# PBB e a Lean Inception

A **Lean Inception** (Paulo Caroli) é um workshop colaborativo de ~1 semana para alinhar um grupo sobre o **MVP** e os incrementos do produto. Ela entende o MVP e suas principais features. O **PBB** cria o backlog de histórias. Juntos, alinham estratégia e entrega.

## Níveis distintos, complementares

- **Lean Inception** responde: *para quando é o MVP? o que é o MVP? estamos alinhados?* → atua no nível de **alinhamento e priorização das features do MVP**.
- **PBB** responde: *quais as histórias da próxima Sprint? estão bem escritas? entendemos o porquê delas?* → atua no nível de **Sprint** e guia o refinamento do backlog.

**Ordem recomendada:** faça a **Lean Inception primeiro, depois o PBB**. Criar backlog sem entender o MVP é arriscado (muito trabalho, baixa eficácia). O PBB é **o passo seguinte da Lean Inception**: quebra as features do MVP em PBIs e escreve as histórias, de forma colaborativa, sem jogar tudo no colo do PO.

## Fazendo o encaixe (reaproveitando artefatos)

O PBB geralmente acontece no **primeiro dia após** a Lean Inception e sai mais rápido porque reaproveita artefatos:

| Bloco do PBB Canvas | De onde vem na Lean Inception |
|---|---|
| **Problemas e Expectativas** | Visão do produto, objetivos, necessidades das personas, resultado esperado (MVP Canvas). Ou deixe vazios — o alinhamento já foi feito. |
| **Personas** | Copie as personas do **MVP Canvas** para o bloco Personas. |
| **Features** | Copie as features do MVP (do **MVP Canvas** ou do **Sequenciador**), **mantendo a ordem do Sequenciador**. Isso já executa a etapa **Ordenar** do COORG. Para cada feature, anote os benefícios/problemas que resolve. |

## Identifique e priorize os PBIs

1. Aplique o **Steps Map** para quebrar cada feature do MVP em PBIs. (Ver `canvas-flow.md`.)
2. Aplique o **COORG** para priorizar e montar um plano de entrega a nível de Sprints. (Ver `coorg.md`.)
3. Escreva os PBIs como **User Stories**. (Ver `user-stories.md`.)

### Priorização dentro de priorização
O **Sequenciador** define a ordem das **features** — muito útil nesse nível. Mas você ainda precisa definir a ordem no nível das **histórias**: aplique o COORG para ordenar as várias histórias das primeiras features.

Depois do COORG nas histórias, verifique **dependências** entre elas (acontece mesmo tentando aplicar INVEST). Se houver, a história dependente recebe automaticamente a mesma pontuação da história de maior valor de que depende. Isso é mais comum com **habilitadores técnicos**, que costumam acompanhar suas respectivas histórias.

> Feitos a Lean Inception e o PBB, o time trabalha com Scrum, Kanban etc. A partir daí: **refinamento contínuo do backlog**, Sprint a Sprint.
