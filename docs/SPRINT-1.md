# Guia da Sprint 1 — DIM0510

Prazo em [CRONOGRAMA.md](CRONOGRAMA.md#visão-geral): entrega em **02/10 (sexta), 23:59**, com apresentações em 28/09 (Coorte B, online) e 30/09 (Coorte A, em sala). O que entregar e como é avaliado: [RUBRICAS.md](RUBRICAS.md#sprint-1). Os enunciados, prontos para virar cartões no quadro, estão em [SPRINT-1-TAREFAS.md](SPRINT-1-TAREFAS.md).

A Sprint 1 é a sprint do **fluxo de trabalho**: a equipe entrega o primeiro incremento funcional e, principalmente, opera o processo que desenhou na Sprint 0 — quadro Kanban com limites de WIP, uma prática de XP de verdade, métricas de fluxo e a primeira retrospectiva com ações.

---

## O que entregar

| Critério da rubrica | Peso | Em uma frase |
|---|---|---|
| Incremento funcional | 30% | Funcionalidade completa na branch principal, executável por terceiros seguindo o README |
| Kanban em uso real | 25% | WIP limits configurados e respeitados, cartões movidos ao longo da sprint, gargalos visíveis |
| Prática XP evidenciada | 20% | ≥ 1 prática XP com evidência no repositório |
| Retrospectiva | 25% | `docs/retrospectiva-01.md` com fatos, causas e ações com responsável e prazo |

Além da entrega técnica, a nota da sprint tem a atividade no repositório (30%) e a comunicação (20%): ver [AVALIACAO.md](AVALIACAO.md#2-nota-de-cada-sprint).

---

## Material de apoio

- Leitura da sprint: [`leituras/processos-s1.md`](../leituras/processos-s1.md) — Lean, Kanban, WIP e Lei de Little (14/09); métricas de fluxo, gestão visual e retrospectivas (21/09).
- Slides: `slides/processos-slides-04.md` (Lean e Kanban) e `slides/processos-slides-05.md` (métricas de fluxo e retrospectivas).
- O acordo de processo da Sprint 0 (`docs/proposta.md`, seção 5): é ele que esta sprint põe à prova.

---

## Incremento funcional

- Uma funcionalidade de ponta a ponta, útil para o usuário do MVP, integrada na branch principal. Melhor uma fatia vertical completa que várias camadas pela metade.
- Qualquer pessoa, seguindo só o `README.md`, consegue rodar: pré-requisitos, comandos e o que esperar.
- A stack é livre; o que conta é funcionar e ser reproduzível.

---

## Kanban em uso real

- As colunas refletem como o trabalho anda de fato. Escrevam no quadro a política de cada coluna: o que precisa ser verdade para um cartão entrar e sair dela.
- Limite de WIP declarado nas colunas de trabalho ("Em progresso", "Em revisão") e respeitado: quando a coluna está cheia, ninguém puxa trabalho novo — ajuda-se a terminar o que está lá.
- Os cartões se movem ao longo da sprint, não só no último dia. O histórico do GitHub Projects e os PRs vinculados mostram isso.
- Gargalos ficam visíveis: cartão parado há dias, coluna sempre cheia, PR esperando revisão. Anotem e tratem na retrospectiva.

---

## Métricas de fluxo

Registrem, para cada cartão concluído, quando o trabalho começou e quando terminou (campos de data no GitHub Projects, ou as datas de abertura e integração dos PRs). Com isso:

| Métrica | O que mede | Como calcular |
|---|---|---|
| Lead time | Do pedido à entrega | Data de chegada ao quadro até "Pronto" |
| Cycle time | Do início do trabalho à entrega | Entrada em "Em progresso" até "Pronto" |
| Throughput | Vazão | Itens concluídos por semana |
| WIP | Trabalho em andamento | Itens entre "Em progresso" e "Pronto" num dado momento |

Levem os números para a retrospectiva e para o vídeo. A Lei de Little (lead time = WIP ÷ throughput) ajuda a explicar por que o limite de WIP encurta o tempo de entrega.

---

## Prática XP evidenciada

Escolham ao menos uma e deixem o rastro no repositório:

| Prática | Evidência |
|---|---|
| Programação em par | Commits com `Co-authored-by:` |
| TDD | Commit do teste antes do commit da implementação, no histórico do PR |
| Refatoração | PRs de refatoração, com testes passando antes e depois |
| Integração contínua | CI em todo PR, branches curtas integradas com frequência |
| Revisão de código | PRs aprovados por outro integrante, com comentários de fato |

Contem na retrospectiva o que funcionou e o que não funcionou com a prática.

---

## Retrospectiva

`docs/retrospectiva-01.md`, escrita ao fim da sprint, com todos:

1. **Fatos**: o que aconteceu, com dados (métricas de fluxo, cartões parados, WIP estourado, PRs sem revisão).
2. **Causas**: por que aconteceu — usem os 5 Porquês nos problemas principais.
3. **Ações**: no máximo três, cada uma com **responsável e prazo**, verificáveis na próxima sprint.
4. **Revisão do acordo de processo**: o que muda no acordo da Sprint 0, se algo mudar.

Impressões genéricas ("comunicação pode melhorar") sem fato, causa e ação não pontuam.

---

## Estrutura do vídeo — 5 minutos

| Tempo | Conteúdo |
|---|---|
| 30 s | O que a sprint entregou |
| 1 min 30 s | O incremento funcionando, a partir do README |
| 1 min 30 s | O quadro: colunas, políticas, WIP e o histórico da sprint; as métricas de fluxo |
| 1 min | A prática XP adotada e a evidência no repositório |
| 30 s | A retrospectiva: o principal problema e as ações |

Todos os integrantes devem falar. Link no `README.md`.

---

## Como o grupo é avaliado nesta sprint

- **Entrega técnica (50%)**: a rubrica da Sprint 1, sobre o estado da branch principal e do quadro no prazo.
- **Atividade no repositório (30%)**: CI verde, commits distribuídos pelas semanas, ao menos um PR integrado por integrante, PRs revisados por outro integrante e cartões do quadro ligados a PRs. O Fator de Participação individual segue [AVALIACAO.md](AVALIACAO.md#32-fator-de-participação).
- **Comunicação (20%)**: média entre o vídeo e a apresentação da coorte.
