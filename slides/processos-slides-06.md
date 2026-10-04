---
marp: true
theme: default
paginate: true
backgroundColor: #ffffff
color: #1a1a2e
style: |
  section {
    font-family: 'Calibri', sans-serif;
    padding: 36px 48px;
    font-size: 1.3em;
  }
  h1 {
    font-family: 'Consolas', monospace;
    color: #1a56db;
    font-size: 1.6em;
    margin-bottom: 0.3em;
    border-bottom: 2px solid #e5e7eb;
    padding-bottom: 0.2em;
  }
  h2 {
    font-family: 'Consolas', monospace;
    color: #374151;
    font-size: 1.2em;
    margin-bottom: 0.25em;
  }
  h3 { color: #6b7280; font-size: 0.9em; margin: 0.2em 0; }
  strong { color: #b45309; }
  em { color: #6b7280; }
  code {
    font-family: 'Consolas', monospace;
    background: #e5e7eb;
    color: #1e3a5f;
    padding: 0.08em 0.3em;
    border-radius: 3px;
    font-size: 1.00em;
  }
  pre {
    background: #f3f4f6 !important;
    border: 1px solid #d1d5db;
    border-left: 3px solid #1a56db;
    border-radius: 6px;
    padding: 0.7em 1em;
    margin: 0.4em 0;
  }
  pre code {
    background: transparent;
    color: #1e3a5f;
    font-size: 0.85em;
    padding: 0;
    line-height: 1.5;
  }
  table { font-size: 0.95em; width: 100%; border-collapse: collapse; }
  th {
    background: #e5e7eb;
    color: #1a56db;
    font-family: 'Consolas', monospace;
    padding: 0.35em 0.7em;
    border: 1px solid #d1d5db;
  }
  td { background: #ffffff; padding: 0.28em 0.7em; border: 1px solid #d1d5db; color: #1a1a2e; }
  tr:nth-child(even) td { background: #f9fafb; }
  ul { margin: 0.25em 0; padding-left: 1.3em; }
  li { margin: 0.18em 0; font-size: 0.88em; line-height: 1.4; }
  blockquote {
    border-left: 3px solid #1a56db;
    background: #eff6ff;
    padding: 0.4em 0.9em;
    margin: 0.5em 0;
    font-style: normal;
    color: #1e3a5f;
    border-radius: 0 5px 5px 0;
    font-size: 1.00em;
  }
  .columns { display: flex; gap: 1.8em; }
  .col { flex: 1; }
  .pill-red   { display:inline-block; background:#fee2e2; border:1.5px solid #dc2626; color:#dc2626; font-family:'Consolas',monospace; font-weight:bold; font-size:0.85em; padding:0.12em 0.6em; border-radius:20px; }
  .pill-green { display:inline-block; background:#dcfce7; border:1.5px solid #16a34a; color:#16a34a; font-family:'Consolas',monospace; font-weight:bold; font-size:0.85em; padding:0.12em 0.6em; border-radius:20px; }
  .pill-blue  { display:inline-block; background:#dbeafe; border:1.5px solid #1a56db; color:#1a56db; font-family:'Consolas',monospace; font-weight:bold; font-size:0.85em; padding:0.12em 0.6em; border-radius:20px; }
  section.lead { justify-content: center; }
  section.lead h1 { font-size: 2.4em; border-bottom: none; }
  section.lead h2 { font-size: 1.5em; color: #6b7280; }
  .tag { display:inline-block; background:#f3f4f6; border:1px solid #d1d5db; color:#374151; font-size:0.85em; padding:0.1em 0.5em; border-radius:4px; font-family:'Consolas',monospace; }


---

# Processos de Software

## O quadro na prática, XP com evidência e a retrospectiva

DIM0510 — Turma 01 · Sprint 1 · parte 2 (vídeo)

Prof. Fernando · UFRN · 2026.2

---

# Errata e novas datas

| Onde | O que muda |
|---|---|
| Cronograma e slides 05 | Entrega da Sprint 1 adiada para **16/10 (sexta), 23:59** |
| Cronograma | A aula de 23/09 foi cancelada; em 28 e 30/09, no lugar das apresentações, houve uma *daily meeting* online com cada grupo. O semestre passa a ter **só mais uma sprint**, a de novembro: ver `docs/CRONOGRAMA.md` |

---

# Onde paramos

```
  14/09 (em sala)   Lean: valor e desperdício · Kanban: fluxo, WIP, Lei de Little
  21/09 (vídeo)     Métricas de fluxo · gestão visual · retrospectivas
```

| Bloco | O que vemos |
|---|---|
| O quadro | Colunas, políticas, limites de WIP, datas e o cartão ligado ao PR |
| Prática XP | Mineração de dados do repositório |
| Medir pelo repositório | uso do `git` e `gh` |
| Retrospectiva | MUSI: fatos, 5 Porquês, ações — e as ações dez dias depois |

---

# Entrega de 16/10 (Sprint 1)

| Critério | Peso | Onde o avaliador olha |
|---|---|---|
| Incremento funcional | 30% | integrado na branch principal, instruções no `README.md` |
| Kanban em uso real | 25% | o quadro: limites, políticas, histórico, cartões ligados a PRs |
| Prática XP evidenciada | 20% | o histórico: commits, PRs, revisões, CI |
| Retrospectiva | 25% | `docs/retrospectiva-01.md` |

> Os quatro critérios são verificados **no repositório e no quadro**: vale o que está registrado lá.

---

<!-- _class: lead -->

# O quadro

## Tornar o trabalho visível, com WIP

---

# Colunas e políticas

```
  Backlog │ Sprint Backlog │ Em progresso (2) │ Em revisão (2) │ Pronto
```

**Política de coluna**, escrita na descrição de cada uma:

```
  Em progresso → Em revisão
    PR aberto · CI verde · a descrição diz como testar

  Em revisão → Pronto
    aprovado por outro integrante · integrado · cartão ligado ao PR
```

📖 **Ref.** `leituras/processos-s1.md`, capítulos 5 e 10

---

# Limite de WIP e datas no GitHub Projects

<div class="columns">
<div class="col">

**Limite por coluna**

- Menu da coluna → limite de itens
- O GitHub mostra p. ex. `2/2` no topo e **destaca** quando estoura
- Coluna cheia → ajudar a terminar antes de puxar novas tarefas

</div>
<div class="col">

**Datas para as métricas**

- Campos de data **Início** e **Fim**, preenchidos ao mover o cartão
- Ou as datas do PR: aberto ≈ início, integrado ≈ fim
- Cartão ligado ao PR: `Closes #12` na descrição do PR
- Automação do projeto: PR integrado → cartão em **Pronto**

</div>
</div>

📖 **Ref.** [GitHub — board layout](https://docs.github.com/en/issues/planning-and-tracking-with-projects/customizing-views-in-your-project/customizing-the-board-layout) · [date fields](https://docs.github.com/en/issues/planning-and-tracking-with-projects/understanding-fields/about-date-fields) · [automações](https://docs.github.com/en/issues/planning-and-tracking-with-projects/automating-your-project/using-the-built-in-automations)

---

<!-- _class: lead -->

# Prática XP

## A evidência que o repositório guarda

---

# Uma prática, com rastro verificável

| Prática | O rastro | Como conferir |
|---|---|---|
| Programação em par | `Co-authored-by:` no commit | `git log --format='%h %s %(trailers:key=Co-authored-by)'` |
| TDD | o commit do teste **antes** do da implementação | a lista de commits do PR |
| Refatoração | PR só de refatoração, testes verdes antes e depois | o PR e o CI |
| Integração contínua | branches curtas, CI em todo PR | `gh pr list --state merged` |
| Revisão de código | PR aprovado por outro integrante, com comentário de fato | a aba *Files changed* |

> `Co-authored-by: Nome <email>` vai no **fim** da mensagem, depois de uma linha em branco. Escolham uma prática e pratiquem **ao longo** da sprint, não na véspera.

📖 **Ref.** [GitHub — commit com vários autores](https://docs.github.com/en/pull-requests/committing-changes-to-your-project/creating-and-editing-commits/creating-a-commit-with-multiple-authors)

---

<!-- _class: lead -->

# Medir pelo repositório

## Quando o quadro não registra

---

# O `gh` devolve o fluxo em JSON

```bash
# cycle time observado: da abertura à integração de cada PR
gh pr list --state merged --json number,createdAt,mergedAt \
  --jq '.[] | "#\(.number): \(((.mergedAt|fromdate) - (.createdAt|fromdate)) / 60 | floor) min"'

# revisões por PR
gh pr list --state merged --json number,reviews --jq '.[] | "#\(.number): \(.reviews | length) revisões"'

# CI: falhas e tempo de retorno
gh run list --json conclusion,createdAt,updatedAt
```

No MUSI, hoje:

```
#5: 36 min        #5: 0 revisões
#1: 48 min        #1: 0 revisões
```

> Menos completo que o quadro — não vê a espera antes de alguém começar —, mas mostra a distância entre o processo **declarado** e o **praticado**.

📖 **Ref.** `leituras/processos-s1.md`, seção 7.6 · [gh pr list](https://cli.github.com/manual/gh_pr_list)

---

<!-- _class: lead -->

# Retrospectiva

## A do MUSI, com os dados reais do projeto

---

# Os fatos

| Fato | Número |
|---|---|
| Cartões no quadro, todos em `Todo` | 3, sem mudança de status em 22 dias |
| Commits direto na `main`, sem PR | 32 de 43 até 19/09 (74%) |
| O PR #1 | integrado em 48 min, sem revisão registrada |
| Colunas e limites que o acordo declara | não existem no quadro |

---

# As causas: cinco porquês

1. Por que nenhum cartão se moveu? — o trabalho começou **no código**, não no cartão
2. Por que no código? — o quadro nasceu depois de 20 dos 43 commits
3. Por que tão tarde? — a urgência era ter o projeto de pé
4. Por que não entrou junto? — para quem tem o plano na cabeça, o quadro não devolvia informação
5. Por que o custo vinha antes? — **o fluxo real não passa pelo quadro** em momento nenhum

> **Causa raiz:** o quadro estava ao lado do trabalho, não no caminho dele. Não foi falta de disciplina — foi intencional para colocar a aplicação de pé, mas agora a ação principal é adotar um conjutno de práticas que coloquem o quadro como artefato principal para interação com o projeto.

---

# As ações — e como estavam dez dias depois

| # | Ação | Prazo | Em 29/09 |
|---|---|---|---|
| A1 | Colunas do acordo, políticas, WIP 2 e 2, cartão por item ligado ao PR | 26/09 | <span class="pill-red">não feita</span> — 3 cartões ainda em `Todo` |
| A2 | Proteger a `main`: PR e CI verde para integrar | 22/09 | <span class="pill-blue">em parte</span> — CI obrigatório, mas PR não exigido |
| A3 | `./verificar.sh` num hook de `pre-push` | 26/09 | <span class="pill-red">não feita</span> |

- Cada ação tem **responsável, prazo e como verificar** — foi isso que permitiu conferir em um minuto
- A próxima retrospectiva **começa por aqui**: por que A1 e A3 não saíram, e por que a A2 ficou pela metade?
- Uma ação com "como medir" pode ser conferida quantitativamente; uma intenção genérica ("melhorar a comunicação"), não

---

# `docs/retrospectiva-01.md` de vocês

1. **Fatos**, com números: lead e cycle time, throughput, WIP estourado, cartões parados, PRs sem revisão
2. **Causas**: 5 Porquês nos problemas principais
3. **Ações**: no máximo três, com **responsável, prazo e como medir**
4. **Revisão do acordo de processo**: o que muda, e por quê

---

# Entrega da Sprint 1 — 16/10, 23:59

| Critério | Peso |
|---|---|
| Incremento funcional em `main`, executável pelo README | 30% |
| Kanban em uso real: WIP configurado e respeitado, gargalos visíveis | 25% |
| ≥ 1 prática XP com evidência no repositório | 20% |
| `docs/retrospectiva-01.md` com fatos, causas e ações com responsável e prazo | 25% |

Guia e tarefas: `docs/SPRINT-1.md` e `docs/SPRINT-1-TAREFAS.md`.

---

# O que muda no semestre

| | Antes | Agora |
|---|---|---|
| Entrega da Sprint 1 | 02/10 | **16/10** (sexta), 23:59 |
| Depois da Sprint 1 | Sprint 2, Sprint 3 e bloco final | **só a Sprint 2**, que é a entrega final, em **30/11** |
| Prova escrita | 21/10 | **09/11** (segunda), em laboratório |
| Prova de reposição | 30/11 | **02/12** (quarta) |
| Fim de cada sprint | apresentação por coorte | ***daily meeting*** online com cada grupo, como em 28 e 30/09 |
| Unidades | três sprints e duas provas espalhadas | U1 = Sprint 0 (30%) + Sprint 1 (70%) · U2 = prova · U3 = Sprint 2 |

- Dentro de cada sprint, **nada muda**: entrega técnica 50%, atividade no repositório 30%, comunicação 20%
- A *daily meeting* entra onde antes entrava a apresentação; as de 28 e 30/09 valeram para a Sprint 1
- Vale a **maior nota** entre a prova e a reposição

> Tudo está em `docs/CRONOGRAMA.md`, `docs/AVALIACAO.md` e `docs/RUBRICAS.md`.

---

# O calendário até dezembro

| Semana | Segunda | Quarta |
|---|---|---|
| 05 e 07/10 | 🟢 em sala: conteúdo da Sprint 1 | 🟢 em sala: conteúdo da Sprint 1 |
| 12 e 14/10 | feriado | 🔵 online: acompanhamento · 🚀 **sexta, 16/10: entrega da Sprint 1** |
| 19 e 21/10 | 🟢 em sala: conteúdo da Sprint 2 | 🟢 em sala: conteúdo da Sprint 2 |
| 26 e 28/10 | 🔵 online: acompanhamento | feriado |
| 02 e 04/11 | feriado | 🔵 online: revisão para a prova |
| 09 e 11/11 | 🟢 em sala: **prova escrita** | 🔵 online: acompanhamento |
| 16 e 18/11 | 🔵 online: acompanhamento | 🟢 em sala: oficina de projeto |
| 23 e 25/11 | 🔵 online: *daily meetings* | 🔵 online: *daily meetings* |
| 30/11 e 02/12 | a definir · 🚀 **entrega final** | 🟢 em sala: **prova de reposição** |

---

# A Sprint 2, a última

| Critério | Peso |
|---|---|
| Pipeline de CI com gate e containerização | 25% |
| Métricas DORA: ≥ 3, com método de coleta reprodutível | 20% |
| Mapeamento de fluxo de valor, com tempos medidos e 1 gargalo com dado | 25% |
| MVP finalizado, com instruções para rodar incluídas no README | 15% |
| Retrospectiva final: as ações da retrospectiva 01 verificadas | 15% |

> O que vocês entregarem em 30/11 é o produto final. A prova de 09/11 cobre as Sprints 0, 1 e 2.

---

# Onde estudar depois

| Fonte | Foco |
|---|---|
| `leituras/processos-s1.md`, cap. 10 | GitHub Projects: quadro, limites, datas, evidência de XP |
| `leituras/processos-s1.md`, 7.6 e 9.5 | Medir pelo repositório · a retrospectiva do MUSI |
| `github.com/fmarquesfilho/musi`, `processo/` | Acordo, métricas e retrospectiva de um projeto real |
| `docs.github.com/en/issues/planning-and-tracking-with-projects` | GitHub Projects |
