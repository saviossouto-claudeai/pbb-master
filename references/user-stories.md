# PBB e História de Usuário

O Scrum não define como representar um item do backlog — pode ser texto livre, caso de uso, modelo ARO ou História de Usuário (o formato mais usado por times ágeis). Cada história é um **lembrete** da necessidade do cliente que provoca a conversa; representa o requisito mais do que o documenta.

> Exemplos abaixo são **originais**, só ilustrativos.

## A conexão PBB → User Story

Depois de preencher o canvas, as histórias saem naturalmente, respondendo 3 perguntas (**3Ws**):

| Pergunta | Vem de… |
|---|---|
| **QUEM?** (who) | a **Persona** |
| **O QUE?** (what) | o **PBI** já escrito em modelo ARO |
| **POR QUÊ?** (why) | o **Benefício** que a persona destacou na feature |

Formato do cartão:
```
Como [PERFIL DA PERSONA]
Posso [FUNÇÃO ESPECÍFICA DO PRODUTO]
Para [VALOR DE NEGÓCIO]
```

## INVEST — regras de uma boa história (Bill Wake)

- **I**ndependente — não depende de outra história.
- **N**egociável — captura a essência do desejado; não é contrato fechado, conversa é bem-vinda.
- **V**aliosa — descreve claramente o valor para o cliente.
- **E**stimável — dá informação suficiente para uma estimativa de alto nível.
- **S**ob medida (Mike Cohn ajustou *small* → *sized appropriately*) — pequena o bastante para caber numa iteração no contexto do time.
- **T**estável — clara o suficiente para que testes possam ser definidos.

## 3Cs — os três elementos (Ron Jeffries)

- **Cartão** — a descrição cabe num cartão índice (Como… Posso… Para…), o suficiente para identificá-la.
- **Conversa** — o cartão é pequeno de propósito; muita conversa é necessária para esclarecer e detalhar. As conversas são **contínuas**, não só no início.
- **Confirmação** — os **critérios de aceite** confirmam que a história foi implementada corretamente. Definidos **antes** de a equipe começar, para não haver surpresas na verificação (geralmente confirmados com o PO).

---

## Habilitadores

Às vezes uma história não sai bem, por mais que se pense em INVEST e 3Cs. Verifique dois casos: (1) ela depende de um **estudo prévio**, ou (2) depende de algo **muito técnico** e de esforço considerável. Nesses casos, separe esse "algo à parte" num **habilitador** — um PBI necessário para habilitar outra história. **Habilitador não segue o formato de história.**

### Habilitador exploratório (Spike)
Realiza pesquisa, atividade prévia, esclarecimento ou escolha entre opções para possibilitar o trabalho numa história. *Spike* é sinônimo comum em times Scrum.

> ❌ "Como desenvolvedor eu quero avaliar bibliotecas de gráficos…" — isso **não** é uma história.
> ✅ Descreva em **ARO**: **"Avaliar as bibliotecas de gráficos disponíveis."** Ele habilita, por ex., a história: *"Como gestora eu quero visualizar o gasto do mês em um gráfico para acompanhar o orçamento."*

### Habilitador técnico
Requisitos não funcionais, refatorações, melhorias no pipeline ou na infra de testes — atividades com esforço alto demais para caber numa história.
- Indique **quais histórias dependem** dele.
- **DICA:** descreva apenas o **"What"** do 3W.
- **Cuidado:** não exagere e acabe com um backlog só de habilitadores.

---

## Critério de Aceite (AC)

Formato textual que descreve **como testar** uma funcionalidade. Uma história tem alguns ACs. Formato Gherkin:
```
Dado que [CENÁRIO INICIAL]
Quando [AÇÃO REALIZADA]
Então [RESULTADO ESPERADO]
```
Os ACs formam a checklist que determina quando a história está concluída e funcionando; geralmente verificados junto ao PO.

**DICA:** se uma história tiver **mais de cinco** critérios de aceite, considere **quebrá-la em duas**.

> Exemplo (original) — História: *Como gestora, Posso aprovar uma despesa pendente, Para liberar o pagamento ao solicitante.*
> - AC 1: **Dado** que a despesa está dentro do meu limite de alçada, **Quando** eu a aprovo, **Então** ela muda para "aprovada" e o solicitante é notificado.
> - AC 2: **Dado** que a despesa excede meu limite, **Quando** tento aprová-la, **Então** o sistema exige a aprovação do nível superior.

## Tarefas

Quebra da história em pedaços técnicos de "como fazer". **Não seguem formato definido** — são diretas, em linguagem técnica, do time de dev para o time de dev. Não são necessariamente independentes nem demonstram valor de negócio. Ex.: "criar endpoint de aprovação", "adicionar campo de limite de alçada no cadastro".

## Interface

Nem todo PBI tem UI. Para os que têm, esclareça a associação com a história. A interface pode ser descrita verbalmente, por sketch, wireframe, mockup ou protótipo — a fidelidade varia por time. O quanto da UI precisa estar pronta para começar é **acordo do time** (parte do Definition of Ready da UI). O importante é o time estar alinhado e confortável.

---

## TAPAs — checando a qualidade das histórias (Manoel Pimentel)

Depois de gerar as histórias, verifique o **alinhamento do time** sobre os atributos principais de cada uma. O TAPAs, criado por Manoel Pimentel, enriquece a análise de 4 atributos:

- **T**angível — a história é tátil, concreta e específica.
- **A**tômica — a história é pequena e independente.
- **P**reciosa — a história resolve um problema importante para o usuário.
- **A**cessível — a história é de claro e fácil entendimento.

A ideia: um bom backlog é como pequenas porções entregues com frequência (Sprint a Sprint), em vez de um grande bloco que demora a ficar pronto.

### Como aplicar
- **TAPAs com cartas** — cada participante recebe uma carta **verde** (atende) e uma **vermelha** (não atende) para cada atributo. A história é apresentada; todos mostram suas cartas para os 4 atributos.
- **TAPAs na matriz** — colunas = Tangível/Atômica/Preciosa/Acessível; linhas = histórias. O time pontua cada célula (verde/vermelho).

### Sinal vermelho — como reduzir os vermelhos
- **Tangível** → seja mais concreto e específico; evite usuários genéricos e descrições abstratas.
- **Atômica** → elimine dependências na forma de implementar; busque implementação auto-contida.
- **Preciosa** → resolva um problema do usuário; descreva o benefício, o porquê.
- **Acessível** → busque solução simples e direta, proporcional ao problema.
