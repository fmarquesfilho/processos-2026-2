# Tarefas da Sprint 1 — DIM0510

Estes são os enunciados das tarefas da Sprint 1, prontos para virar cartões no GitHub
Projects. Cada um tem um objetivo, o que fazer, e o *pronto quando* alinhado à rubrica.

O **como** está em [SPRINT-1.md](SPRINT-1.md) e na leitura da sprint
([`leituras/processos-s1.md`](../leituras/processos-s1.md)) — as tarefas apontam para a seção
certa em vez de repeti-la. Os pesos vêm de [RUBRICAS.md](RUBRICAS.md#sprint-1). Prazo em
[CRONOGRAMA.md](CRONOGRAMA.md#visão-geral): **02/10, 23:59**.

| # | Tarefa | Critério da rubrica |
|---|---|---|
| T1 | Planejar a sprint no quadro | Kanban em uso real (25%) |
| T2 | Escrever as políticas das colunas e os limites de WIP | Kanban em uso real (25%) |
| T3 | Entregar o incremento funcional | Incremento funcional (30%) |
| T4 | Adotar uma prática XP com evidência | Prática XP evidenciada (20%) |
| T5 | Registrar as métricas de fluxo | Kanban em uso real (25%) · Retrospectiva (25%) |
| T6 | Conduzir e registrar a retrospectiva | Retrospectiva (25%) |
| T7 | Gravar o vídeo de 5 minutos e preparar a apresentação | Comunicação |

---

## T1 — Planejar a sprint no quadro

**Objetivo.** Comprometer só o que cabe na sprint, com dono.

**O que fazer.**
- [ ] Mover para "Sprint Backlog" as histórias P1 que formam o incremento
- [ ] Quebrar as histórias grandes em cartões que caibam em poucos dias
- [ ] Atribuir um responsável a cada cartão

**Pronto quando.** O "Sprint Backlog" tem as histórias do incremento, quebradas e com dono, no início da sprint.

**Referência.** [SPRINT-1.md](SPRINT-1.md) *Incremento funcional* · `processos-s1.md`, capítulo 4.

---

## T2 — Escrever as políticas das colunas e os limites de WIP

**Objetivo.** Transformar o quadro de lista em sistema puxado.

**O que fazer.**
- [ ] Escrever, na descrição de cada coluna, o critério para entrar e sair dela
- [ ] Declarar o limite de WIP de "Em progresso" e "Em revisão" (no nome ou na descrição da coluna)
- [ ] Combinar o que fazer quando a coluna enche: ajudar a terminar antes de puxar
- [ ] Atualizar o acordo de processo, se os limites mudarem

**Pronto quando.** Toda coluna tem política escrita e as colunas de trabalho têm WIP declarado e respeitado.

**Referência.** [SPRINT-1.md](SPRINT-1.md) *Kanban em uso real* · `processos-s1.md`, capítulos 5 e 6.

---

## T3 — Entregar o incremento funcional

**Objetivo.** Uma funcionalidade completa, rodando para qualquer pessoa.

**O que fazer.**
- [ ] Implementar a fatia vertical escolhida, de ponta a ponta
- [ ] Integrar na branch principal por PR, com revisão de outro integrante
- [ ] Escrever no `README.md` como rodar: pré-requisitos, comandos, o que esperar
- [ ] Pedir a alguém de fora da equipe que siga o README do zero

**Pronto quando.** A funcionalidade está na branch principal e roda seguindo só o README.

**Referência.** [SPRINT-1.md](SPRINT-1.md) *Incremento funcional*.

---

## T4 — Adotar uma prática XP com evidência

**Objetivo.** Praticar XP de fato, com rastro verificável.

**O que fazer.**
- [ ] Escolher ≥ 1 prática (par, TDD, refatoração, integração contínua, revisão)
- [ ] Registrar no acordo de processo como a equipe vai aplicá-la
- [ ] Deixar a evidência no repositório (`Co-authored-by:`, teste antes da implementação, PRs de refatoração)

**Pronto quando.** A prática aparece no histórico do repositório ao longo da sprint, não só no fim.

**Referência.** [SPRINT-1.md](SPRINT-1.md) *Prática XP evidenciada* · [AVALIACAO.md](AVALIACAO.md#33-integridade) (`Co-authored-by`).

---

## T5 — Registrar as métricas de fluxo

**Objetivo.** Medir como o trabalho andou, com números.

**O que fazer.**
- [ ] Registrar a data de início e de fim de cada cartão (campos de data do GitHub Projects ou datas dos PRs)
- [ ] Calcular, ao fim da sprint, lead time e cycle time médios, throughput por semana e o WIP médio
- [ ] Apontar o cartão que mais demorou e onde ele ficou parado
- [ ] Registrar os números na retrospectiva

**Pronto quando.** Há lead time, cycle time e throughput calculados a partir de dados do quadro, e eles aparecem na retrospectiva.

**Referência.** [SPRINT-1.md](SPRINT-1.md) *Métricas de fluxo* · `processos-s1.md`, capítulo 7.

---

## T6 — Conduzir e registrar a retrospectiva

**Objetivo.** Aprender com a sprint e mudar algo concreto na próxima.

**O que fazer.**
- [ ] Reunir todos, com as métricas e o quadro abertos
- [ ] Levantar fatos, discutir causas (5 Porquês nos problemas principais)
- [ ] Definir no máximo três ações, cada uma com responsável e prazo
- [ ] Registrar em `docs/retrospectiva-01.md` e criar cartões para as ações

**Pronto quando.** `docs/retrospectiva-01.md` tem fatos com dados, causas discutidas e ações com responsável e prazo.

**Referência.** [SPRINT-1.md](SPRINT-1.md) *Retrospectiva* · `processos-s1.md`, capítulo 8.

---

## T7 — Gravar o vídeo de 5 minutos e preparar a apresentação

**Objetivo.** Mostrar o incremento e, principalmente, o processo em funcionamento.

**O que fazer.**
- [ ] Seguir o roteiro do guia (incremento · quadro e métricas · prática XP · retrospectiva)
- [ ] Garantir que **todos os integrantes falam**
- [ ] Publicar o vídeo e linkar no `README.md`
- [ ] Ensaiar a apresentação da coorte (28/09 online ou 30/09 em sala)

**Pronto quando.** O vídeo tem ~5 min, cobre o roteiro, todos falam, e está acessível pelo link.

**Referência.** [SPRINT-1.md](SPRINT-1.md) *Estrutura do vídeo* · [AVALIACAO.md](AVALIACAO.md#4-componente-c--comunicação).
