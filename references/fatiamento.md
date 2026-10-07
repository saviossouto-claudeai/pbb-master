# Fatiamento vertical — quebrar PBIs e histórias sem perder valor

> **Técnica complementar ao PBB.** O livro usa o Steps Map para quebrar uma **feature** em PBIs. Esta referência cobre o passo seguinte do dia a dia: quebrar um **PBI ou história que ainda está grande demais**, mantendo cada pedaço com valor próprio e potencialmente utilizável. Ao usar, diga ao usuário que é uma técnica complementar, não parte do método PBB.
>
> Fontes: SPIDR (Mike Cohn), padrões de divisão de histórias (Richard Lawrence / Humanizing Work), Hamburger Method (Gojko Adzic), Elephant Carpaccio (Alistair Cockburn) e *right-sizing* pelo SLE (Daniel Vacanti). Exemplos **originais**.

---

## Steps Map × fatiamento

| | Steps Map (PBB) | Fatiamento vertical (complementar) |
|---|---|---|
| Entrada | Uma **feature** | Um **PBI ou história** grande demais |
| Pergunta | "Quais os passos do fluxo de trabalho?" | "Qual a menor versão disso que alguém já usaria?" |
| Saída | PBIs em ARO | Histórias menores, cada uma com valor e critérios de aceite |
| Risco | Passos que sozinhos não servem a ninguém | Fatias tão finas que viram tarefas |

Os dois se completam: Steps Map primeiro (feature → PBIs); depois, o **teste da fatia** em cada PBI. Os que falharem por tamanho, fatie; os que falharem por valor, junte com o vizinho ou refaça o corte.

---

## O teste da fatia

Aplique a cada pedaço (PBI, história ou fatia proposta). As perguntas 1 e 2 são eliminatórias.

| # | Pergunta | Se não… |
|---|---|---|
| 1 | **Utilizável:** se só esta fatia ficar pronta, alguma persona consegue usar ou ver o resultado? | Não é fatia, é tarefa ou camada. Junte com o vizinho ou refaça o corte. |
| 2 | **Valor validável:** o PO consegue demonstrar e aprender algo com ela (na review, com um usuário real)? | Idem. |
| 3 | **Vertical:** atravessa todas as camadas necessárias (tela, regra, dado) para funcionar? | Cortaram por camada. Refaça por comportamento. |
| 4 | **Testável:** tem critérios de aceite próprios, de no máximo 5? | Mais de 5 → fatie de novo (cada regra ou cenário é candidato a fatia). Nenhum → falta conversa com o PO. |
| 5 | **Cabe no SLE:** o time acredita que termina dentro do SLE (ex.: "85% dos itens em até 8 dias")? | Grande demais. Fatie de novo. Sem SLE definido: "termina em poucos dias?" |

> **Right-sizing (Vacanti):** a pergunta 5 dispensa estimativa em pontos. Não é "quanto vale?", é "provavelmente cabe no nosso SLE?". Sim → pode entrar. Não → fatiar. Isso respeita o PBB, que não estima esforço. Se o time usa a skill one-page-report, o SLE é o **Cycle Time P85** que ela calcula.

**"Potencialmente utilizável" não é "completo".** Uma primeira fatia que aceita só um tipo de despesa, só um canal ou só o caminho feliz é utilizável por parte dos usuários e já gera aprendizado. Isso é valor. O que não serve é "criar a tabela" ou "fazer a tela": ninguém usa isso sozinho.

---

## Sinais de que o item precisa ser fatiado

- Mais de 5 critérios de aceite.
- "e" / "ou" na história ("Posso cadastrar **e** editar **e** excluir…").
- Verbos genéricos: gerenciar, controlar, manter, administrar.
- Mais de uma persona, canal ou tipo de dado no mesmo item.
- Muitas regras de negócio ou exceções.
- O time não consegue dizer se cabe no SLE, ou diz claramente que não cabe.
- Itens que ficam no Aging WIP acima do P85 com frequência: sinal de que o refinamento está deixando passar itens grandes.

---

## Padrões de fatiamento (SPIDR + complementos)

Tente nesta ordem e pare no primeiro que gerar fatias que passem no teste.

| Padrão | Como cortar | Pergunta para o PO |
|---|---|---|
| **Caminhos (Paths)** | Um fluxo alternativo por fatia. O caminho feliz mais simples primeiro, exceções depois | "Qual o caminho mais comum? Os outros podem vir depois?" |
| **Regras (Rules)** | Primeira fatia com a regra mais simples (ou sem a regra); cada regra de negócio vira fatia | "Que regra podemos simplificar ou adiar na primeira versão?" |
| **Dados (Data)** | Um tipo, formato ou faixa de dado por fatia (ex.: só reais, depois moeda estrangeira) | "Qual tipo de dado cobre a maioria dos casos?" |
| **Interfaces** | Um canal ou dispositivo por fatia; ou interface simples primeiro, versão rica depois | "Qual canal os usuários mais usam hoje?" |
| **Operações** | Separar criar / consultar / editar / excluir quando "gerenciar" esconde várias ações | "O que o usuário precisa fazer primeiro?" |
| **Simples / complexo** | Versão mínima funcional primeiro; variações e refinamentos depois | "Qual a menor versão disso que alguém já usaria?" |
| **Adiar qualidade não funcional** | Funciona primeiro; performance, escala ou volume depois, como fatia própria | "Precisamos de toda a performance já na primeira versão?" |
| **Spike** | Quando a incerteza impede fatiar: um habilitador exploratório (ARO) para aprender, depois fatiar | "O que precisamos descobrir antes de saber como cortar?" |

**Hamburger (Gojko Adzic)**, para itens muito técnicos: liste as etapas (camadas) do item; para cada uma, liste opções da mais simples à mais completa; a primeira fatia é a opção mais simples de cada camada, atravessando todas. As fatias seguintes melhoram uma camada por vez.

---

## Anti-padrões — não são fatias

- **Por camada:** "fazer o front", "fazer a API", "criar o banco". São tarefas (ver `user-stories.md`), não itens de backlog.
- **Por fase:** "analisar", "desenvolver", "testar". Isso é processo, não valor.
- **Por pessoa ou especialidade:** "parte do João", "parte do QA".
- **Fatia sem critérios de aceite próprios:** se não dá para testar isoladamente, não é independente.
- **Fatiar só para caber na Sprint, sem olhar valor:** pedaços pequenos que ninguém usa aumentam o WIP e não reduzem o risco.

---

## Como conduzir (Agile Master apoiando o PO)

1. **Entenda o item:** persona, valor (o "Para…") e critérios de aceite atuais. Se faltar o valor, pergunte antes de fatiar; sem ele não dá para avaliar o teste da fatia.
2. **Diagnostique:** quais sinais de tamanho aparecem? Rode o teste da fatia no item inteiro.
3. **Proponha 2 ou 3 formas de cortar** (padrões diferentes), cada uma com as fatias resultantes. O PO escolhe. Quem decide o valor e a ordem é ele.
4. **Escreva as fatias** como histórias (3Ws) com critérios de aceite (Dado/Quando/Então).
5. **Rode o teste da fatia em cada uma** e mostre o resultado. Fatia que falha em 1 ou 2: junte ou refaça.
6. **Sugira a primeira fatia:** a que entrega mais aprendizado com menos esforço, normalmente o caminho feliz mais simples de ponta a ponta.
7. **Diga "NÃO" com o PO:** algumas fatias de baixo valor talvez nem devam ser feitas. Fatiar revela isso.

---

## Exemplo (original)

**Item grande:** *Como colaborador solicitante, Posso solicitar o reembolso das minhas despesas, Para receber de volta o que gastei a trabalho.*
Critérios atuais: 9 (várias moedas, limite por categoria, foto do comprovante, despesa com vários itens, app e web, aprovação em dois níveis…). Sinais: mais de 5 ACs, muitas regras, dois canais.

**Corte proposto (Caminhos + Regras + Dados):**

| # | Fatia | Utilizável? | Cabe no SLE? |
|---|---|---|---|
| 1 | Solicitar reembolso de **uma** despesa em reais, com foto do comprovante, pela web | ✅ Solicitante já pede; gestor já recebe | ✅ |
| 2 | Aplicar o limite por categoria na solicitação | ✅ Evita pedidos fora da política | ✅ |
| 3 | Solicitar reembolso com **vários itens** no mesmo pedido | ✅ Atende viagens | ✅ |
| 4 | Solicitar reembolso em **moeda estrangeira** | ✅ Atende quem viaja para fora | ⚠️ Depende da fonte de câmbio → spike antes |
| 5 | Solicitar reembolso pelo **app** | ✅ Novo canal | ✅ |

Habilitador exploratório antes da fatia 4: **"Avaliar as fontes de cotação de câmbio disponíveis."** (ARO, não história).

**Corte ruim (por camada):** "criar tabela de reembolso", "criar tela de solicitação", "criar API de envio". Nenhum passa no teste 1.

**Fatia 1 como história:**
> Como colaborador solicitante
> Posso solicitar o reembolso de uma despesa em reais com a foto do comprovante
> Para receber de volta o que gastei a trabalho
>
> - **Dado** que preenchi valor, data, categoria e anexei a foto, **Quando** envio a solicitação, **Então** ela fica "pendente" e aparece para meu gestor.
> - **Dado** que não anexei a foto, **Quando** tento enviar, **Então** o sistema pede o comprovante.
