# Backlog Ready e Refinamento Contínuo

## Definição de Preparado (DoR) e de Pronto (DoD)

A qualidade de um PBI é medida na **entrada** e na **saída** de uma Sprint.

> **Só deixe ENTRAR na Sprint o que estiver READY; só deixe SAIR o que estiver DONE.**

### Definition of Ready (DoR)
Acordo entre time e PO que indica quando um PBI está **preparado** para ser puxado para uma Sprint — tem informação suficiente para planejamento, execução e entrega. Costuma indicar que o time:
- tem a informação necessária para trabalhar no item;
- entende o porquê do item;
- consegue reconhecer quando o trabalho termina;
- sabe como o item se relaciona com uma feature;
- concorda que o item cabe em uma Sprint.

Cada equipe define e mantém sua própria checklist de DoR. Um exemplo de itens que uma checklist pode conferir: o PBI é representado por uma User Story (3Ws), preserva o INVEST, está coberto por critérios de aceite, está mapeado para uma interface e passou por um check de qualidade (ex.: TAPAs). (DoR é útil também em Kanban, não só Scrum.)

### Definition of Done (DoD)
Acordo que demonstra a qualidade do PBI produzido — "Done" comprova a satisfação de todos com o trabalho. Um PBI que não atende o DoD **não** deve ser liberado nem apresentado na Sprint review; permanece como WIP. Cada equipe define sua própria checklist; itens comuns: entrega um incremento do produto, cumpre os critérios de aceite, está documentado para uso, adere aos padrões de código e mantém os indicadores de performance.

---

## Refinamento Contínuo

Refinamento = **quebrar features** ou **incluir informação adicional** aos PBIs para ter itens menores e mais precisos (descrição, ordem, tamanho). O DoR é o guia do refinamento.

**Refine só as próximas 1–3 Sprints.** Um time na Sprint N refina para a N+1. Não refine antecipadamente itens de um futuro distante — isso é o oposto do ágil (projetos não ágeis refinavam tudo antes de desenvolver tudo). Pense em planejar uma **trilha ajustável, não um trilho fixo**: caminhe um pouco, observe o feedback, ajuste e siga.

O PBB é útil no dia a dia, não só no início: ajuda a **estruturar** o backlog num refinamento contínuo, incorporando novas necessidades a partir de insights e feedback dos usuários. A cada entrega, o time (1) **estrutura** o backlog convertendo feedback/insight em features/PBIs e (2) **reordena** com os novos PBIs (via COORG).

---

## Estruturar o backlog — transformar feedback/insight em item

Verifique se o feedback/insight é um **PBI** ou uma **feature**:

### Feedback que vira PBI — 3 cenários
Associe o PBI a uma feature e, por consequência, a uma persona:
1. **Feature e persona já existem** → associe o PBI à feature (que já está ligada a uma persona).
2. **Feature não existe, persona existe** → crie a feature, associe-a à persona existente e faça o entendimento dela (problemas e benefícios).
3. **Nem feature nem persona existem** → crie a feature e a persona, e faça o entendimento da feature (problemas e benefícios). Não precisa descrever o que a persona faz/espera, pois você já tem a feature definida.

### Feedback que vira Feature — 2 cenários
Associe a feature a uma persona:
1. **Persona já existe** → associe a nova feature à persona existente.
2. **Persona não existe** → crie a persona e associe a feature a ela (não precisa descrever o que ela faz/espera).

Depois: faça o **entendimento** (problemas e benefícios) da feature e aplique o **Steps Map** para quebrá-la em PBIs.

### Atualizar (re-priorizar) o backlog
Classifique os novos PBIs para compará-los aos existentes; ordene conforme a feature; re-organize o backlog inteiro segundo a pontuação de todos (novos + antigos). Ver `coorg.md`.

---

## Uso típico no arranque

Muitos times fazem uma sessão de PBB na **Sprint 0** (set-up/preparação), refinando o trabalho para as Sprints 1, 2 e 3. O PBB dá o senso de direção inicial; após Steps Map + COORG, selecionam-se os itens mais prioritários para refinar e desenvolver. Daí em diante: refinamento contínuo, Sprint a Sprint.
