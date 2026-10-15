# Guia da Sprint 2 — DIM0510

Prazo em [CRONOGRAMA.md](CRONOGRAMA.md#visão-geral): entrega final em **30/11 (segunda), 23:59**. Conteúdo em 19 e 21/10; acompanhamento online em 26/10, 09/11 e 16/11; *daily meetings* online em 23 e 25/11 (presencial em 18/11, para quem avisar antes). O que entregar e como é avaliado: [RUBRICAS.md](RUBRICAS.md#sprint-2). Os enunciados, prontos para virar cartões no quadro, estão em [SPRINT-2-TAREFAS.md](SPRINT-2-TAREFAS.md).

A Sprint 2 é a última do semestre: o que for entregue em 30/11 é o produto final. É a sprint da **automação e do fluxo de valor**: o pipeline passa a ser o portão de entrada da branch principal, o projeto sobe com `docker compose`, e a equipe mede, com números tirados do próprio repositório, como entrega e onde o trabalho espera.

---

## O que entregar

| Critério da rubrica | Peso | Em uma frase |
|---|---|---|
| Pipeline de CI e containerização | 25% | Build, testes e lint em todo push e PR; verde na branch principal; portão que impede merge com falha; `docker compose up` do zero |
| Métricas DORA | 20% | Ao menos 3 métricas tiradas do repositório, com método descrito e reprodutível, e interpretação |
| Mapeamento de Fluxo de Valor | 25% | O fluxo real com tempos medidos, eficiência de fluxo, 1 gargalo com número e 1 melhoria com métrica-alvo |
| MVP finalizado | 15% | Os fluxos do MVP de ponta a ponta; README que roda em menos de 10 min; licença |
| Retrospectiva final | 15% | `docs/retrospectiva-02.md`: as ações da retrospectiva 01 conferidas, a evolução com dados e o uso de IA avaliado |

Além da entrega técnica, a nota da sprint tem a atividade no repositório (30%) e a comunicação (20%): ver [AVALIACAO.md](AVALIACAO.md#2-nota-de-cada-sprint).

---

## Material de apoio

- Leitura da sprint: [`leituras/processos-s2.md`](../leituras/processos-s2.md) — DevOps, integração contínua, o portão e containers (19/10); métricas DORA e mapeamento do fluxo de valor (21/10).
- Slides: `slides/processos-slides-08.md` (19/10) e `slides/processos-slides-09.md` (21/10).
- O MUSI (`github.com/fmarquesfilho/musi`): o workflow do CI, a proteção da branch e os números DORA usados como exemplo nos slides de 21/10.
- Um `docker compose` completo: `web2-2026-2/exemplos/compose.yaml` (banco, um serviço em Go e uma API, com health checks).
- A leitura de dívida técnica (`leituras/processos-s1-divida-tecnica.md`): as dívidas registradas podem aparecer no mapa do fluxo e na retrospectiva.

---

## Pipeline de CI e containerização

- O workflow roda **build, testes e lint** em todo push e em todo pull request.
- A branch principal está protegida: PR obrigatório, o job do CI como status check obrigatório, valendo para administradores.
- O portão foi provado: um PR que quebra um teste fica bloqueado. Guardem o link desse PR (ou um print) como evidência.
- O CI está verde na branch principal no prazo.
- `docker compose up` sobe o projeto do zero, numa máquina que só tem Docker: sem instalar a linguagem, sem passos manuais. Health checks e `depends_on` com `service_healthy` quando houver mais de um serviço.

---

## Métricas DORA

- Escrevam primeiro **o que é uma implantação** no projeto e como ela é contada (cada push na branch principal, cada release, cada execução do job de publicação; ou, se o projeto não está no ar, cada merge com CI verde).
- Ao menos **três** das cinco métricas: tempo de espera da mudança, frequência de implantação, tempo de recuperação, taxa de falha de mudança, taxa de retrabalho.
- Para cada uma: a definição usada, os **comandos exatos** (`gh`, `git`), o período, o valor e a limitação da fonte. Outra pessoa deve conseguir repetir e chegar ao mesmo número.
- A **interpretação**: o que os números dizem do processo, e o que não dizem. Mostrem a distribuição (por semana, por PR), não só a média.
- Em `docs/metricas-02.md` (ou outro nome, citado no README).

---

## Mapeamento de Fluxo de Valor

- O desenho do fluxo **real**, da ideia ao "no ar": as etapas do quadro e as que o quadro não mostra (espera por revisão, espera pelo merge, a implantação).
- Para ao menos três itens concluídos: o tempo de processamento e o de espera de cada etapa, com a **fonte** de cada número (datas do quadro, do PR, do CI). Tempos estimados aparecem marcados como estimados, com o método.
- O lead time e a **eficiência de fluxo** (tempo de processamento ÷ lead time) de cada item, e a média. Digam se as horas são corridas ou úteis.
- **Um gargalo sustentado por número** e **uma melhoria com métrica-alvo**: a mudança no processo, o responsável, o prazo e o número que vai mostrar se melhorou.
- Em `docs/fluxo-de-valor.md` (ou outro nome, citado no README), com o diagrama (Mermaid, imagem ou texto).

---

## MVP finalizado

- Os fluxos do MVP funcionam de ponta a ponta.
- README que permite a terceiros rodar o projeto em menos de 10 minutos.
- Licença definida.

---

## Retrospectiva final

- `docs/retrospectiva-02.md`.
- **As ações da retrospectiva 01, conferidas com evidência**: para cada uma, foi feita? Como se verifica? Se não foi, por quê?
- **A evolução do processo**, da Sprint 1 ao fim, com dados: as métricas de fluxo da Sprint 1 ao lado das métricas DORA e do mapa desta sprint.
- **O uso de IA**, a partir do registro em `docs/uso-de-ia.md`: onde ajudou, onde atrapalhou, o que a equipe faria diferente.
- Fatos, causas e até três ações, como na retrospectiva 01, agora para um próximo projeto.

---

## Estrutura do vídeo — 5 minutos

| Tempo | Conteúdo |
|---|---|
| 30 s | O que a sprint entregou |
| 1 min | O pipeline: um PR bloqueado pelo portão e o CI verde na branch principal |
| 1 min | `docker compose up` do zero e o MVP funcionando |
| 1 min 30 s | As métricas DORA e o mapa do fluxo: o gargalo e a melhoria |
| 1 min | A retrospectiva final: o que mudou no processo, com números |

Todos os integrantes devem falar. Link no `README.md`.

---

## Como o grupo é avaliado nesta sprint

- **Entrega técnica (50%)**: a rubrica da Sprint 2, sobre o estado da branch principal no prazo (hash do último commit).
- **Atividade no repositório (30%)**: CI verde, commits distribuídos pelas semanas, ao menos um PR integrado por integrante, PRs revisados por outro integrante e cartões do quadro ligados a PRs. O Fator de Participação individual segue [AVALIACAO.md](AVALIACAO.md#32-fator-de-participação).
- **Comunicação (20%)**: média entre o vídeo e a *daily meeting* (23 ou 25/11, online, ou 18/11, em sala).
