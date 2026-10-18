# Tarefas da Sprint 2 — DIM0510

Estes são os enunciados das tarefas da Sprint 2, prontos para virar cartões no GitHub Projects. Cada um tem um objetivo, o que fazer, e o *pronto quando* alinhado à rubrica.

O **como** está em [SPRINT-2.md](SPRINT-2.md) e na leitura da sprint ([`leituras/processos-s2.md`](../leituras/processos-s2.md)): as tarefas apontam para a seção certa em vez de repeti-la. Os pesos vêm de [RUBRICAS.md](RUBRICAS.md#sprint-2). Prazo em [CRONOGRAMA.md](CRONOGRAMA.md#visão-geral): **30/11, 23:59**.

| # | Tarefa | Critério da rubrica |
|---|---|---|
| T1 | Planejar a sprint no quadro e começar a medir | Atividade no repositório · DORA (20%) · Fluxo de valor (25%) |
| T2 | Completar o workflow de CI | Pipeline de CI e containerização (25%) |
| T3 | Proteger a branch principal e provar o portão | Pipeline de CI e containerização (25%) |
| T4 | Subir o projeto com `docker compose` | Pipeline de CI e containerização (25%) |
| T5 | Coletar e interpretar as métricas DORA | Métricas DORA (20%) |
| T6 | Mapear o fluxo de valor | Mapeamento de Fluxo de Valor (25%) |
| T7 | Testar uma melhoria e medir o efeito | Mapeamento de Fluxo de Valor (25%) |
| T8 | Finalizar o MVP | MVP finalizado (15%) |
| T9 | Conduzir e registrar a retrospectiva final | Retrospectiva final (15%) |
| T10 | Gravar o vídeo de 5 minutos | Comunicação |

> Projeto de referência: `github.com/fmarquesfilho/musi`, pastas `processo/` e `.github/workflows/`.

---

## T1 — Planejar a sprint no quadro e começar a medir

**Objetivo.** Ter o histórico de que as métricas e o mapa vão precisar.

**O que fazer.**
- [ ] Criar os cartões das tarefas T2 a T10 e das histórias que faltam no MVP, com responsável
- [ ] Preencher os campos Início e Fim de cada cartão, sempre
- [ ] Definir o que é uma implantação no projeto
- [ ] Combinar como registrar o tempo de processamento de alguns itens (quem fez anota, no fim do dia)

**Pronto quando.** O quadro tem os cartões com dono e datas, e a definição de implantação está escrita.

**Referência.** `processos-s2.md`, capítulos 6.3 e 8.2.

---

## T2 — Completar o workflow de CI

**Objetivo.** O CI confere build, testes e lint, em todo push e PR.

**O que fazer.**
- [ ] Conferir os gatilhos: `push` na branch principal e `pull_request`
- [ ] Rodar build, testes e lint, com os mesmos comandos que a equipe usa localmente
- [ ] Manter o CI rápido (minutos)
- [ ] Deixar o CI verde na branch principal

**Pronto quando.** Em todo push e PR, o CI roda build, testes e lint, e está verde na branch principal.

**Referência.** `processos-s2.md`, capítulo 3.

---

## T3 — Proteger a branch principal e provar o portão

**Objetivo.** Nenhum código que quebra os testes entra na branch principal.

**O que fazer.**
- [ ] Em *Settings → Branches* (ou *Rules*): PR obrigatório, o job do CI como status check obrigatório, valendo para administradores
- [ ] Conferir com `gh api repos/<dono>/<repo>/branches/main/protection`
- [ ] Abrir um PR que quebra um teste, de propósito, e confirmar que o merge fica bloqueado
- [ ] Guardar o link do PR como evidência no README ou no `docs/`

**Pronto quando.** A proteção está ativa para todos, e há um PR que mostra o bloqueio.

**Referência.** `processos-s2.md`, capítulo 4.

---

## T4 — Subir o projeto com `docker compose`

**Objetivo.** O projeto sobe do zero, numa máquina que só tem Docker.

**O que fazer.**
- [ ] Escrever o `Dockerfile` de cada componente do projeto
- [ ] Escrever o `compose.yaml`, com health checks e `depends_on: service_healthy` quando houver mais de um serviço
- [ ] Testar num clone limpo
- [ ] Atualizar o README e a definição de pronto

**Pronto quando.** Num clone limpo, `docker compose up --build` sobe o projeto, sem passos manuais.

**Referência.** `processos-s2.md`, capítulo 5 · `web2-2026-2/exemplos/compose.yaml`.

---

## T5 — Coletar e interpretar as métricas DORA

**Objetivo.** Três métricas, com método reprodutível e interpretação.

**O que fazer.**
- [ ] Escrever a definição de implantação e como ela é contada
- [ ] Escolher ao menos três métricas e, para cada uma, a definição, os comandos, o período, o valor e a limitação
- [ ] Mostrar a distribuição (por semana, por PR), além da média
- [ ] Interpretar: o que os números dizem do processo, e o que não dizem
- [ ] Registrar em `docs/metricas-02.md`

**Pronto quando.** Outra pessoa consegue repetir os comandos e chegar aos mesmos números, e a interpretação explica o que eles mostram.

**Referência.** `processos-s2.md`, capítulo 6.

---

## T6 — Mapear o fluxo de valor

**Objetivo.** Saber, com números, onde o trabalho da equipe espera.

**O que fazer.**
- [ ] Desenhar as etapas reais, da ideia ao "no ar", inclusive as que o quadro não mostra
- [ ] Escolher três itens concluídos e anotar, por etapa, o tempo de processamento e o de espera, com a fonte
- [ ] Calcular o lead time e a eficiência de fluxo de cada item e a média; dizer se as horas são corridas ou úteis
- [ ] Apontar o gargalo, com o número que o mostra
- [ ] Registrar em `docs/fluxo-de-valor.md`, com o diagrama

**Pronto quando.** O mapa tem os tempos medidos, com fonte, a eficiência calculada e um gargalo sustentado por número.

**Referência.** `processos-s2.md`, capítulo 7.

---

## T7 — Testar uma melhoria e medir o efeito

**Objetivo.** Uma mudança no processo, com número para saber se funcionou.

**O que fazer.**
- [ ] Escolher uma melhoria que ataca o gargalo da T6, com responsável e prazo
- [ ] Definir a métrica-alvo (a mesma que mostrou o gargalo) e o valor esperado
- [ ] Aplicar a melhoria por pelo menos uma semana
- [ ] Medir de novo e registrar o resultado, mesmo que não tenha melhorado

**Pronto quando.** O documento do fluxo tem a melhoria, a métrica-alvo, e o valor antes e depois.

**Referência.** `processos-s2.md`, capítulo 7.4.

---

## T8 — Finalizar o MVP

**Objetivo.** O produto que a equipe se propôs a entregar, funcionando.

**O que fazer.**
- [ ] Completar os fluxos do MVP e testá-los de ponta a ponta
- [ ] README: pré-requisitos, como rodar (com o `docker compose`), o que esperar
- [ ] Escolher e acrescentar a licença
- [ ] Pedir a alguém de fora do grupo que siga o README e cronometrar

**Pronto quando.** Uma pessoa de fora roda o MVP em menos de 10 minutos.

**Referência.** [RUBRICAS.md](RUBRICAS.md#sprint-2) *MVP finalizado*.

---

## T9 — Conduzir e registrar a retrospectiva final

**Objetivo.** Olhar o semestre com dados e aprender com ele.

**O que fazer.**
- [ ] Conferir cada ação da retrospectiva 01, com a evidência combinada na época
- [ ] Comparar o processo da Sprint 1 com o do fim, com números (métricas de fluxo, DORA, o mapa)
- [ ] Avaliar o uso de IA a partir de `docs/uso-de-ia.md`
- [ ] Fatos, causas e até três ações para um próximo projeto
- [ ] Registrar em `docs/retrospectiva-02.md`

**Pronto quando.** O documento confere as ações anteriores com evidência, mostra a evolução com dados e avalia o uso de IA.

**Referência.** `processos-s2.md`, capítulo 8 · `processos-s1.md`, capítulo 9.

---

## T10 — Gravar o vídeo de 5 minutos

**Objetivo.** Mostrar o produto e o processo, com números.

**O que fazer.**
- [ ] Seguir o roteiro do guia (o pipeline e o portão · o compose e o MVP · DORA e o fluxo · a retrospectiva)
- [ ] Garantir que **todos os integrantes falam**
- [ ] Publicar o vídeo e linkar no `README.md`
- [ ] Mostrar o andamento na *daily meeting* do grupo (23 ou 25/11, ou 18/11 em sala)

**Pronto quando.** O vídeo tem cerca de 5 min, cobre o roteiro, todos falam, e está acessível pelo link.

**Referência.** [SPRINT-2.md](SPRINT-2.md) *Estrutura do vídeo* · [AVALIACAO.md](AVALIACAO.md#4-componente-c--comunicação).
