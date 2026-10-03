# Rúbricas — DIM0510 Processos de Software

**Período**: 2026.2

Os critérios de todas as entregas estão disponíveis desde o início do semestre, o que permite adiantar trabalho.

Prazos e datas: [CRONOGRAMA.md](CRONOGRAMA.md#visão-geral). Pesos e regras de nota: [AVALIACAO.md](AVALIACAO.md).

---

## Como ler as rúbricas

Cada critério é avaliado em quatro níveis:

| Nível | Nota | Significado |
|-------|------|-------------|
| **Excelente** | 10 | Atende plenamente e demonstra domínio |
| **Bom** | 8 | Atende, com lacunas menores |
| **Suficiente** | 6 | Atende no mínimo aceitável |
| **Insuficiente** | 0–4 | Não atende ou está ausente |

O Componente A (entrega técnica, 50%) é a média ponderada dos critérios da sprint. O Componente B (30%) segue [AVALIACAO.md §3](AVALIACAO.md#3-componente-b--atividade-no-repositório). O Componente C (20%) usa a rúbrica de comunicação ao final deste documento.

---

## Sprint 0

Templates, exemplos e estrutura do vídeo e da proposta: [SPRINT-0.md](SPRINT-0.md).

| Critério | Peso | Excelente (10) | Suficiente (6) | Insuficiente (0–4) |
|----------|------|----------------|----------------|--------------------|
| **Definição do problema** | 25% | Problema real, delimitado, com público-alvo identificado e evidência de que existe | Problema plausível mas genérico | Problema vago ou ausente |
| **Escopo do MVP** | 25% | MVP viável em 4 sprints, com critérios de "pronto" explícitos e fora-de-escopo declarado | MVP descrito mas sem limites claros | Escopo irreal ou indefinido |
| **Backlog inicial** | 25% | ≥ 5 itens no GitHub Projects, escritos como resultado para o usuário, ≥ 3 estimados, priorizados | ≥ 5 itens listados, priorização frágil | < 5 itens ou lista de tarefas técnicas sem valor de usuário |
| **Configuração do processo** | 25% | Repositório público, README completo, quadro Kanban criado com colunas e WIP declarado, papéis do Scrum atribuídos, coorte declarada | Repositório e quadro criados, configuração incompleta | Repositório privado, sem quadro ou sem README |

---

## Sprint 1

| Critério | Peso | Excelente (10) | Suficiente (6) | Insuficiente (0–4) |
|----------|------|----------------|----------------|--------------------|
| **Incremento funcional** | 30% | Funcionalidade completa em `main`, executável por terceiros seguindo o README | Funcionalidade parcial, executa com ajustes | Não executa ou nada entregue |
| **Kanban em uso real** | 25% | WIP limits configurados e respeitados, cartões movidos ao longo da sprint, gargalos visíveis no quadro | Quadro usado, WIP declarado mas não respeitado | Quadro estático ou atualizado só no fim |
| **Prática XP evidenciada** | 20% | ≥ 1 prática XP adotada com evidência no repo (testes escritos antes, `Co-authored-by` em pair, histórico de refatoração) | Prática mencionada, evidência fraca | Sem evidência |
| **Retrospectiva** | 25% | `docs/retrospectiva-01.md` com fatos observados, causas discutidas e **ações com responsável e prazo** | Retrospectiva registra impressões, sem ações concretas | Ausente ou genérica |

---

## Sprint 2

Última sprint do semestre (ajuste de 03/10): substitui a Sprint 2, a Sprint 3 e a Entrega Final previstas no início do período. O que for entregue aqui é o produto final.

| Critério | Peso | Excelente (10) | Suficiente (6) | Insuficiente (0–4) |
|----------|------|----------------|----------------|--------------------|
| **Pipeline de CI e containerização** | 25% | Workflow roda build, testes e lint em todo push e PR, verde em `main`, com gate impedindo merge com falha; `docker compose up` sobe o projeto do zero | CI sem gate, ou compose incompleto | Sem CI, CI vermelho ou sem Docker |
| **Métricas DORA** | 20% | Ao menos 3 métricas coletadas do próprio repositório, com **método de coleta descrito e reprodutível**, e interpretação | Métricas coletadas, método vago | Métricas ausentes ou inventadas |
| **Mapeamento de Fluxo de Valor** | 25% | Diagrama do pipeline real com tempos de processamento e de espera medidos, eficiência de fluxo calculada, ao menos 1 gargalo sustentado por número e 1 melhoria com métrica-alvo | Diagrama presente, tempos estimados sem base | Diagrama genérico ou ausente |
| **MVP finalizado** | 15% | Fluxos do MVP funcionam ponta a ponta; README permite a terceiros rodar em menos de 10 min; licença definida | Produto roda com instruções incompletas | Não roda |
| **Retrospectiva final** | 15% | `docs/retrospectiva-02.md` verifica as ações da retrospectiva 01 com evidência, mostra a evolução do processo da Sprint 1 ao fim com dados e avalia o uso de IA registrado em `docs/uso-de-ia.md` | Retrospectiva descritiva, sem dados | Ausente ou genérica |

---

## Rúbrica de Comunicação (Componente C, 20% de toda sprint)

| Critério | Peso | Excelente (10) | Suficiente (6) | Insuficiente (0–4) |
|----------|------|----------------|----------------|--------------------|
| **Clareza e objetividade** | 30% | Mensagem direta, dentro do tempo, sem enrolação | Mensagem compreensível, tempo estourado ou subutilizado | Confusa ou muito fora do tempo |
| **Demonstração** | 30% | Mostra o produto/artefato funcionando, não slides sobre ele | Demonstração parcial | Só slides |
| **Evidência** | 25% | Afirmações sustentadas por dados do próprio projeto | Afirmações genéricas | Afirmações sem base |
| **Participação da equipe** | 15% | Todos os integrantes falam sobre o que fizeram | Maioria participa | Um só fala pelo grupo |

A rubrica vale para o vídeo e para a *daily meeting*, que não exige slides nem preparação: conta o que o grupo mostra e explica. Nas *daily meetings*, o docente pode dirigir perguntas a qualquer integrante sobre qualquer parte da entrega. A incapacidade de explicar a própria contribuição afeta o Fator de Participação individual.

---

## Checklist por sprint

Pode ser copiado para o `README.md` do repositório.

```markdown
### Sprint 0
- [ ] Repositório público + README completo
- [ ] docs/proposta.md (≤3 pág.)
- [ ] GitHub Projects com ≥5 itens, ≥3 estimados
- [ ] Coorte declarada (A=presencial / B=online)
- [ ] Integração com outra disciplina declarada (se houver)
- [ ] Vídeo 5 min

### Sprint 1
- [ ] Incremento funcional em main
- [ ] Kanban com WIP limits configurados
- [ ] Evidência de prática XP
- [ ] docs/retrospectiva-01.md com ações
- [ ] Vídeo 5 min

### Sprint 2 (final)
- [ ] CI verde (build + testes + lint) com gate em PR
- [ ] Dockerfile + docker-compose.yml: sobe do zero
- [ ] docs/dora.md com ≥3 métricas e o método de coleta
- [ ] docs/vsm.md com tempos medidos, 1 gargalo com dado e 1 melhoria com métrica-alvo
- [ ] MVP ponta a ponta; README roda em menos de 10 min
- [ ] docs/retrospectiva-02.md verificando as ações da retrospectiva 01
- [ ] Vídeo 5 min
```
