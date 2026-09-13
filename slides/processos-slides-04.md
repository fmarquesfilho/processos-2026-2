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

## Lean e Kanban

DIM0510 — Turma 01 · Sprint 1 · 14/09

Prof. Fernando · UFRN · 2026.2

---

# Roteiro da semana

**Segunda, 14/09 — Lean e Kanban**

| Bloco | O que vemos |
|---|---|
| Lean | Origem, pilares, valor e desperdício |
| 7 desperdícios · 7 princípios | O Lean traduzido para software |
| Kanban | Princípios, práticas e sistema puxado |
| WIP e Lei de Little | Por que limitar trabalho acelera a entrega |

**Quarta, 16/09 — Acompanhamento online** (projeto)
**Segunda, 21/09** — Métricas de fluxo, retrospectivas e **oficina do quadro**

> Do Scrum (ritmo por sprints) para o **fluxo**: como o trabalho anda, e por que às vezes ele empaca.

---

# Onde paramos

Na Sprint 0 vimos como **organizar** o trabalho:

```
  Scrum: papéis, cerimônias e artefatos
  Backlog: histórias INVEST, fatiamento vertical, DoD
  XP: práticas técnicas, TDD, pair programming
```

Hoje mudamos a pergunta: não "como nos organizamos em ciclos", mas **"como o valor flui — e onde ele trava"**. É a lente do Lean.

---

<!-- _class: lead -->

# Lean

## Assista o bastão, não os corredores

---

# De onde vem o Lean

- Nasce no **Toyota Production System (TPS)**, pós-Segunda Guerra
- De sistema de produção a **filosofia de gestão**
- Popularizado pelo MIT nos anos 90 (*lean*)
- Aplicado muito além da fábrica: produtos, serviços, **TI**

> Princípio central: **foco no fluxo de valor**. O cliente define o que é valor — todo o resto é candidato a desperdício.

---

# Os dois pilares

<div class="columns">
<div class="col">

## Respeito pelas pessoas

- Desenvolver pessoas antes de produtos
- Times auto-organizados
- Gestores como **professores-mentores**

</div>
<div class="col">

## Melhoria contínua (Kaizen)

- Desafiar o status quo
- Pequenas melhorias, sempre
- Cultura de experimentação

</div>
</div>

> "O fracasso é não tentar melhorar." O Lean é **cultura**, não um conjunto de ferramentas soltas.

---

# Valor e desperdício

O objetivo é entregar valor de forma **sustentável**: menor *lead time*, mais qualidade, menor custo, alta moral.

Três fontes de desperdício:

| Termo | O que é | Em TI |
|---|---|---|
| **Muda** | Atividade sem valor | Retrabalho, espera, feature inútil |
| **Mura** | Variabilidade | Lotes irregulares, picos de demanda |
| **Muri** | Sobrecarga | Prazos irreais, pessoa gargalo |

> Reduzir Muda sem tratar Mura e Muri é enxugar gelo.

---

# Os 7 desperdícios do software

Poppendieck traduz os desperdícios da fábrica para o desenvolvimento:

| # | Desperdício | Exemplo no projeto |
|---|---|---|
| 1 | Trabalho parcial | Branch aberta há semanas, sem integrar |
| 2 | Funcionalidades extras | Recurso que ninguém pediu |
| 3 | Reaprendizado | Redescobrir o que já se sabia |
| 4 | Transferências | Repassar tarefa entre pessoas |
| 5 | Espera / atrasos | PR parado esperando revisão |
| 6 | Troca de tarefas | Pular entre 3 histórias ao mesmo tempo |
| 7 | Defeitos | Bug que volta da "coluna pronto" |

> Guardem o item 6. Ele é a ponte para o **WIP** do Kanban.

---

# Os 7 princípios do Lean para software

| # | Princípio | Em uma frase |
|---|---|---|
| 1 | Eliminar desperdício | Tudo que não agrega valor ao cliente |
| 2 | Construir qualidade | Qualidade embutida, não inspecionada no fim |
| 3 | Criar conhecimento | O código e o processo ensinam o time |
| 4 | Adiar compromissos | Decidir no último momento responsável |
| 5 | Entregar rápido | Ciclos curtos, feedback cedo |
| 6 | Respeitar as pessoas | Quem faz o trabalho decide como fazê-lo |
| 7 | Otimizar o todo | O sistema inteiro, não partes isoladas |

> "Adiar compromissos" não é procrastinar: é **decidir com mais informação**, mais tarde.

---

# Duas ferramentas do Lean

<div class="columns">
<div class="col">

## 5 Porquês

Perguntar "por quê?" ao menos cinco vezes até a **causa raiz**.

Aplicar no *Gemba* — onde o trabalho acontece, com observação direta.

</div>
<div class="col">

## PDCA

```
Plan  → Do
  ↑         ↓
Act   ← Check
```

Ciclo de melhoria: planejar, fazer, medir, ajustar. Kaizen em movimento.

</div>
</div>

> Melhoria contínua não é evento: é hábito, sustentado por dados.

---

<!-- _class: lead -->

# Kanban

## Tornar o trabalho visível, e limitá-lo

---

# O que é Kanban

Um método para **gerir o fluxo** de trabalho — evolucionário, não revolucionário.

- Começa **de onde você já está** (nada de reorganizar tudo)
- Busca **mudança incremental** e contínua
- Respeita papéis e processos atuais
- Vem do **sistema puxado** do Lean: produzir sob demanda, não empurrar

> Não é o quadro por si. É o quadro **com limites e políticas** — sem isso, é só uma lista bonita.

---

# Os 4 princípios fundamentais

1. **Comece com o que você faz hoje** — sem ruptura
2. **Concorde em buscar mudança incremental** e evolutiva
3. **Respeite** papéis, responsabilidades e cargos atuais
4. **Incentive a liderança** em todos os níveis

> É por isso que Kanban "cabe" em qualquer time — inclusive por cima do Scrum de vocês.

---

# As 6 práticas centrais

| # | Prática | O que significa |
|---|---|---|
| 1 | Visualizar o fluxo | Um quadro que mostra o trabalho real |
| 2 | Limitar o WIP | Um teto de itens em progresso |
| 3 | Gerir o fluxo | Observar e suavizar o movimento |
| 4 | Tornar políticas explícitas | O que significa "pronto" em cada coluna |
| 5 | Implementar feedback | Cadências de revisão (ex.: retrospectiva) |
| 6 | Melhorar colaborativamente | Evoluir por experimentos |

---

# Prática 1 — visualizar o fluxo

O quadro espelha **como o trabalho realmente anda**:

```
  A fazer   │  Fazendo   │  Revisão   │  Pronto
 ───────────┼────────────┼────────────┼──────────
  #12       │  #7        │  #4        │  #1
  #15       │  #9        │            │  #2
  #18       │            │            │  #3
```

- No GitHub Projects: colunas = etapas reais (não "genéricas")
- Cada cartão é uma história/tarefa, ligada a um PR
- **Gestão visual**: gargalo vira óbvio (coluna lotada)

> "Fazendo" com 8 cartões e "Revisão" vazia conta uma história — e não é boa.

---

# Prática 2 — limitar o WIP

<div class="columns">
<div class="col">

**Sem limite** <span class="pill-red">empurra</span>

```
Fazendo (WIP 6)
 #7 #9 #11 #13 #15 #17
 tudo começado,
 nada termina
```

</div>
<div class="col">

**Com limite** <span class="pill-green">puxa</span>

```
Fazendo (máx 3)
 #7 #9 #11
 só puxa novo
 quando um sai
```

</div>
</div>

Limitar o WIP ataca o **desperdício nº 6** (troca de tarefas) e o **nº 1** (trabalho parcial): expõe gargalos, revela defeitos cedo, permite decidir mais tarde.

> O limite não é punição. É o que **força** o time a terminar antes de começar.

---

# A Lei de Little

A relação que sustenta o limite de WIP:

```
  Lead Time  =  WIP  ÷  Throughput
```

- **WIP**: itens em progresso
- **Throughput**: itens concluídos por unidade de tempo
- **Lead Time**: tempo do início ao fim de um item

**Exemplo.** 12 itens em progresso, terminando 3 por semana:

```
  Lead Time = 12 ÷ 3 = 4 semanas
```

> Metade do WIP, mesmo throughput → **metade do lead time**. É por isso que limitar WIP acelera a entrega.

---

# Práticas 3 a 6

| Prática | No projeto de vocês |
|---|---|
| Gerir o fluxo | Olhar onde os cartões param, semana a semana |
| Políticas explícitas | Escrever o "pronto" de cada coluna no quadro |
| Feedback | Retrospectiva ao fim da sprint (21/09) |
| Melhorar juntos | Ajustar limites e colunas por experimento |

> Políticas implícitas geram discussão sem fim. Escritas no quadro, viram acordo.

---

# Kanban e Scrum não brigam

| | Scrum | Kanban |
|---|---|---|
| Cadência | Sprints fixas | Fluxo contínuo |
| Papéis | Definidos | Mantém os atuais |
| Mudança | Por sprint | Incremental, contínua |
| Limite | Escopo da sprint | WIP por coluna |

> No projeto vocês usam os dois: o **ritmo** do Scrum e o **fluxo** do Kanban sobre o mesmo quadro.

---

# Erros comuns

- Focar só na **ferramenta** (o quadro) sem mudar a cultura
- Quadro sem **limite de WIP** — vira lista de tarefas
- Colunas genéricas que não refletem o trabalho real
- Políticas na cabeça de um, não escritas
- Esperar resultado imediato — Lean é jornada

> "Adotar Kanban" sem limitar WIP é pendurar um quadro na parede e seguir empurrando.

---

# No projeto de vocês

Olhem o próprio quadro com estas perguntas:

- As colunas refletem como o trabalho **de fato** anda?
- Qual seria um **limite de WIP** honesto para "Fazendo"?
- O que significa "pronto" em cada coluna?
- Onde os cartões **ficam parados** com mais frequência?
