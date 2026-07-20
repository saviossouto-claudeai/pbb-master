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
