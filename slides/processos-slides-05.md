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

## Métricas de fluxo e retrospectivas

DIM0510 — Turma 01 · Sprint 1 · 21/09

Prof. Fernando · UFRN · 2026.2

---

# Roteiro da semana

**Segunda, 21/09 — Medir o fluxo e aprender com ele**

| Bloco | O que vemos |
|---|---|
| Métricas de fluxo | Lead time, cycle time, throughput, WIP |
| Ler os números | Média, distribuição, idade do item, CFD |
| Gestão visual | Sinais de gargalo no quadro |
| Retrospectivas | Estrutura, formatos, fatos → causas → ações |
| Oficina | Quadro, limites de WIP, primeira retrospectiva |

**Quarta, 23/09 — Acompanhamento online** (projeto)
**28 e 30/09 — Apresentações** · 🚀 **Entrega da Sprint 1: 02/10, 23:59**

---

# Onde paramos

Em 14/09, a lente do Lean e o Kanban:

```
  Valor e desperdício: muda, mura, muri
  7 desperdícios · 7 princípios no software
  Kanban: visualizar, limitar o WIP, gerir o fluxo
  Lei de Little: lead time = WIP ÷ throughput
```

Hoje: **medir** o fluxo e transformar o que foi medido em **mudança**.

---

<!-- _class: lead -->

# Métricas de fluxo

## Números em vez de impressões

---

# As quatro métricas

| Métrica | Pergunta | Unidade |
|---|---|---|
| **Lead time** | Quanto o cliente espera, do pedido à entrega? | dias |
| **Cycle time** | Quanto o trabalho leva, do início à entrega? | dias |
| **Throughput** | Quantos itens terminamos por período? | itens/semana |
| **WIP** | Quantos itens estão em andamento agora? | itens |

```
  entrou no quadro ──── espera ────▶ início ──── trabalho ────▶ pronto
  └──────────────────────── lead time ─────────────────────────┘
                                     └──────── cycle time ──────┘
```

> Escolham os pontos de início e fim, escrevam no acordo e usem sempre os mesmos.

---

# Um exemplo com seis cartões

| Cartão | Entrou | Início | Pronto | Lead | Cycle |
|---|---|---|---|---|---|
| #1 | 14/09 | 15/09 | 17/09 | 3 | 2 |
| #2 | 14/09 | 15/09 | 22/09 | 8 | 7 |
| #3 | 14/09 | 18/09 | 23/09 | 9 | 5 |
| #4 | 16/09 | 22/09 | 24/09 | 8 | 2 |
| #5 | 16/09 | 23/09 | 29/09 | 13 | 6 |
| #6 | 21/09 | 24/09 | 30/09 | 9 | 6 |

- Lead médio **8,3 dias** · cycle médio **4,7 dias** → **3,7 dias parados** antes de começar
- Throughput por semana: **1 · 3 · 2**

> A primeira semana quase não entregou. Pergunta para a retrospectiva: **por quê?**

---

# Além da média

<div class="columns">
<div class="col">

## Distribuição

- O #2 levou 7 dias: mais que o dobro da maioria
- Gráfico de dispersão: conclusão × cycle time
- Percentil: "85% ficam prontos em até N dias"

</div>
<div class="col">

## Idade do item

- Lead e cycle só existem **depois** que termina
- Durante a sprint: **há quantos dias** está em andamento?
- Mais velho que o normal da equipe → agir **agora**

</div>
</div>

> Médias escondem justamente os casos que mais incomodam.

---

# Lei de Little, de novo

```
  WIP médio = throughput × tempo médio
```

No exemplo: 6 itens em 19 dias (≈ 0,32/dia) × 4,7 dias ≈ **1,5 item** em andamento, em média.

| WIP | Throughput | Tempo médio |
|---|---|---|
| 12 | 3/semana | 4 semanas |
| 6 | 3/semana | **2 semanas** |

- Vale para **médias** de um sistema **estável**
- Explica tendências; **não** promete a data de um item

---

# Diagrama de fluxo cumulativo (CFD)

```
 itens
   │                                  ░░░░ Pronto
   │                        ░░░░░░░░░░▒▒▒▒ Em revisão
   │              ░░░░░░░░░░▒▒▒▒▒▒▒▒▒▒▓▓▓▓ Em progresso
   │    ░░░░░░░░░░▒▒▒▒▒▒▒▒▒▒▓▓▓▓▓▓▓▓▓▓████ Sprint Backlog
   └──────────────────────────────────────▶ dias
```

- Distância **vertical** entre faixas: o WIP do dia
- Distância **horizontal**: o tempo na etapa
- Faixa que **engorda**: gargalo (entra mais do que sai)
- Inclinação de "Pronto": o throughput

> À mão: uma contagem por coluna por dia, numa planilha, gráfico de área empilhada.

---

<!-- _class: lead -->

# Gestão visual

## O quadro como radiador de informação

---

# Sinais de gargalo

| No quadro | Costuma significar |
|---|---|
| "Em revisão" sempre cheia | Revisão é o gargalo: revisar vira prioridade |
| Cartão com a mesma pessoa há dias | Grande demais, ou bloqueado sem aviso |
| "Em progresso" acima do limite | Limite não respeitado, ou irreal |
| Cartões voltando de "Pronto" | Definição de Pronto frouxa |
| "Sprint Backlog" que não diminui | Compromisso maior que a capacidade |

> O gargalo define a vazão do sistema inteiro. Acelerar outra etapa só aumenta a fila na frente dele.

---

# Políticas explícitas

Escritas na descrição de cada coluna:

```
  Em progresso → Em revisão
    PR aberto · CI verde · descrição diz como testar

  Em revisão → Pronto
    aprovado por outro integrante · integrado · cartão ligado ao PR
```

- Encerram a discussão "isso já está pronto?"
- Tornam a Definição de Pronto **verificável**
- Cartão bloqueado fica **marcado**, com o motivo

---

<!-- _class: lead -->

# Retrospectivas

## Inspecionar e adaptar o processo

---

# Cinco etapas

*Derby & Larsen, Agile Retrospectives*

| # | Etapa | Na prática |
|---|---|---|
| 1 | Preparar o terreno | Objetivo e combinado: foco no processo, não nas pessoas |
| 2 | Coletar dados | Quadro e métricas abertos; fatos |
| 3 | Gerar entendimento | Causas: **5 Porquês** |
| 4 | Decidir o que fazer | Poucas ações |
| 5 | Encerrar | Registrar e combinar o acompanhamento |

Formatos para coletar: **Começar/parar/continuar** · **4Ls** · **Veleiro** (vento, âncora, rochas). Mais em `retromat.org`.

---

# Fatos → causas → ações

```markdown
## Fatos
- Cycle time médio de 4,7 dias; o cartão #2 levou 7.
- "Em revisão" passou do limite (3) em 4 dos 15 dias úteis.

## Causas
- O #2 misturava tela e integração; grande demais.
- Pedidos de revisão só na notificação do GitHub.

## Ações
- Quebrar histórias > 3 dias antes de puxar — Ana — início da Sprint 2
- Pedir revisão no grupo, com o link do PR — todos; Bruno acompanha — a partir de 05/10
```

> "Melhorar a comunicação" não é ação. **Até três ações, com responsável e prazo.**

---

# Erros comuns na retrospectiva

- Impressões sem fato, causa ou ação ("foi corrido")
- Ações sem responsável: de todos = de ninguém
- Não revisar as ações da retrospectiva anterior
- Discutir pessoas em vez do processo
- Retrospectiva que não muda nada no acordo de processo

---

# Entrega da Sprint 1 — 02/10, 23:59

| Critério | Peso |
|---|---|
| Incremento funcional em `main`, executável pelo README | 30% |
| Kanban em uso real: WIP configurado e respeitado, gargalos visíveis | 25% |
| ≥ 1 prática XP com evidência no repositório | 20% |
| `docs/retrospectiva-01.md` com fatos, causas e ações com responsável e prazo | 25% |

Guia e tarefas: `docs/SPRINT-1.md` e `docs/SPRINT-1-TAREFAS.md`. Apresentações: 28/09 (Coorte B, online) e 30/09 (Coorte A, em sala).

---

# Próximas aulas

- **23/09** — acompanhamento online: tragam o quadro com limites e as primeiras datas
- **28 e 30/09** — apresentações da Sprint 1
- **05/10** — Sprint 2: cultura DevOps (CALMS, Três Caminhos), CI/CD com GitHub Actions
- **07/10** (online) — Docker, Infrastructure as Code, métricas DORA e SPACE

---

# Onde estudar depois

| Fonte | Foco |
|---|---|
| `leituras/processos-s1.md` | A Sprint 1 inteira, com exemplos e exercícios |
| `kanbanguides.org` | The Kanban Guide |
| Vacanti · *Actionable Agile Metrics for Predictability* | Métricas de fluxo |
| Derby & Larsen · *Agile Retrospectives* | Retrospectivas |
| `retromat.org` | Atividades para cada etapa |
