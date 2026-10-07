# Template de export em markdown

Gere o export seguindo esta estrutura. Preencha só o que a sessão produziu — omita seções vazias. Este export é para colar no Jira / Azure DevOps / Notion; mantenha-o limpo e sem enfeites.

```markdown
# PBB — [Nome do Produto]

## Contexto
**Problemas (estado atual):**
- …

**Expectativas (estado desejado):**
- …

## Personas
- **[Persona]** — faz: [atividade]; espera: [desejo]

## Features (máx. 10, na ordem do COORG)
| # | Feature | Persona | Problemas que resolve | Benefícios |
|---|---------|---------|-----------------------|------------|
| 1 | …       | …       | …                     | …          |

## Backlog priorizado (COORG)
Critérios usados: [ex.: Frequência de uso (1–5) + Valor de negócio (1–3)] · Fórmula: [ex.: soma]

| Prio | PBI (modelo ARO) | Feature | [Critério 1] | [Critério 2] | Total |
|------|------------------|---------|--------------|--------------|-------|
| 1    | Efetuar a compra do livro | Realizar compra online | 5 | 3 | 8 |

_Itens abaixo do corte (PO disse "NÃO"):_ [listar ou "nenhum"]

## User Stories
### US-01 — [título curto]
> Como [persona]
> Posso [função — PBI em ARO]
> Para [valor/benefício]

**Critérios de aceite:**
- Dado que [cenário], Quando [ação], Então [resultado]

**Habilitadores (se houver):** [ARO — ex.: "Realizar pesquisa de mensageria assíncrona" (spike)]
**Interface:** [verbal / sketch / wireframe / mockup / protótipo / n/a]
**Tarefas (opcional):** …

## TAPAs (opcional)
| História | Tangível | Atômica | Preciosa | Acessível |
|----------|----------|---------|----------|-----------|
| US-01    | ✅ | ✅ | ✅ | ⚠️ |
```

Regras:
- PBIs **sempre** em modelo ARO (verbo no início).
- User Stories **sempre** no formato Como/Posso/Para (3Ws).
- Critérios de aceite **sempre** em Dado/Quando/Então; se passarem de 5, sinalize que a história deveria ser quebrada.
- Não invente pontuações COORG — use as definidas com o usuário.

---

# Modelos curtos — uso pontual (modo 0)

Use só o bloco da prática pedida. Sem canvas, sem seções vazias.

### Fatiamento
```markdown
**Item original:** Como [persona], Posso [função], Para [valor]
**Por que fatiar:** [sinais: 9 ACs, 3 regras, 2 canais…]

**Opção A — [padrão, ex.: Caminhos + Regras]**
| # | Fatia (história) | Utilizável | Valor validável | Vertical | ACs ≤ 5 | Cabe no SLE |
|---|---|---|---|---|---|---|
| 1 | … | ✅ | ✅ | ✅ | ✅ | ✅ |

**Opção B — [outro padrão]** …

**Sugestão de primeira fatia:** [#] — [motivo em uma linha]. A decisão é do PO.
**Habilitadores:** [ARO, se houver]

### US-01 — [título]
> Como … / Posso … / Para …
- Dado que …, Quando …, Então …
```

### Revisão de histórias (INVEST + TAPAs)
```markdown
| História | I | N | V | E | S | T | Problema | Correção sugerida |
|---|---|---|---|---|---|---|---|---|
| US-01 | ✅ | ✅ | ⚠️ | ✅ | ❌ | ✅ | Valor não explícito; grande demais | Explicitar o "Para…"; fatiar por regra |
```

### Definition of Ready
```markdown
**Item:** [título] — **Ready? Não** (2 lacunas)
| Critério do DoR | Status | Pergunta para fechar |
|---|---|---|
| História em 3Ws | ✅ | — |
| Critérios de aceite | ❌ | "O que acontece quando…?" |
```

### COORG rápido
```markdown
Critérios: [critério (escala)] + [critério (escala)] · Fórmula: [soma] · _validar com o PO_
| Ordem | PBI (ARO) | [C1] | [C2] | Total |
|---|---|---|---|---|
_Abaixo do corte (sugestão de "NÃO"):_ …
```
