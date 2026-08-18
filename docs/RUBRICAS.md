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
| **Backlog inicial** | 25% | ≥ 10 itens no GitHub Projects, escritos como resultado para o usuário, ≥ 3 estimados, priorizados | ≥ 10 itens listados, priorização frágil | < 10 itens ou lista de tarefas técnicas sem valor de usuário |
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

| Critério | Peso | Excelente (10) | Suficiente (6) | Insuficiente (0–4) |
|----------|------|----------------|----------------|--------------------|
| **Pipeline de CI** | 30% | Workflow roda build + testes + lint em todo push e PR, verde em `main`, com gate impedindo merge com falha | Workflow roda build e testes, sem gate | Sem CI ou CI vermelho |
| **Containerização** | 25% | `docker compose up` sobe o projeto inteiro do zero; imagem com build multi-estágio e sem segredos | Dockerfile funciona, compose incompleto | Sem Docker ou não executa |
| **Métricas DORA** | 30% | As 5 métricas coletadas do próprio repositório, com **método de coleta descrito e reprodutível**, e interpretação do arquétipo do time | 3+ métricas coletadas, método vago | Métricas ausentes ou inventadas |
| **Incremento funcional** | 15% | Segundo incremento entregue e integrado | Incremento parcial | Nada novo entregue |

---

## Sprint 3

| Critério | Peso | Excelente (10) | Suficiente (6) | Insuficiente (0–4) |
|----------|------|----------------|----------------|--------------------|
| **Mapeamento de Fluxo de Valor (VSM) do estado atual** | 30% | Diagrama do pipeline real com tempos de processamento e de espera medidos, e cálculo da eficiência de fluxo | Diagrama presente, tempos estimados sem base | Diagrama genérico ou ausente |
| **Gargalos com dados** | 25% | ≥ 2 gargalos identificados, cada um sustentado por número extraído do próprio projeto | Gargalos identificados por percepção | Sem identificação de gargalos |
| **Propostas de melhoria** | 20% | 1–2 melhorias com métrica-alvo, valor atual, valor esperado e como será verificado | Melhorias descritas sem métrica | Ausente ou genérica |
| **Revisão de código** | 15% | ≥ 3 PRs com revisão substantiva (comentários que mudaram o código), critérios de revisão documentados | PRs aprovados sem comentários | Sem revisão |
| **Evolução DORA** | 10% | Comparação Sprint 2 → Sprint 3 com gráfico e interpretação | Números comparados sem análise | Ausente |

---

## Entrega Final

Esta entrega absorve o conteúdo do bloco final: topologias de equipe, engenharia de plataformas, IA em processos e melhoria contínua.

| Critério | Peso | Excelente (10) | Suficiente (6) | Insuficiente (0–4) |
|----------|------|----------------|----------------|--------------------|
| **MVP finalizado** | 20% | Todos os fluxos do MVP funcionam ponta a ponta; CI verde; README permite a terceiros rodar em menos de 10 min; licença definida | Produto roda com instruções incompletas | Não roda |
| **Relatório final** | 25% | Narrativa da evolução do processo com evidências: VSM final, DORA com gráficos, decisões e efeitos medidos, comparação da Sprint 1 ao fim | Relatório descritivo, evidências parciais | Relatório genérico |
| **Proposta de melhoria de processo** | 20% | Diagnóstico com dados, proposta, métrica de sucesso e plano de implantação com riscos, fundamentados em conceitos do curso | Proposta plausível, fundamentação fraca | Proposta genérica ou sem dados |
| **Análise de topologia** | 15% | Equipe classificada nos tipos estudados, modos de interação identificados, Lei de Conway aplicada ao próprio produto | Classificação feita sem análise | Ausente |
| **Uso crítico de IA** | 10% | `docs/uso-de-ia.md` registra ferramentas, tarefas e avaliação de impacto no processo, com evidência | Registro descritivo, sem análise | Ausente |
| **Análise crítica e rastreabilidade** | 10% | Lições aprendidas conectadas aos conceitos do curso, reconhecendo o que não funcionou e por quê; artefatos do semestre presentes e coerentes | Lições superficiais ou artefatos inconsistentes | Ausente ou autoelogiosa |

---

## Rúbrica de Comunicação (Componente C, 20% de toda sprint)

Aplica-se ao vídeo e, quando houver, à apresentação ao vivo.

| Critério | Peso | Excelente (10) | Suficiente (6) | Insuficiente (0–4) |
|----------|------|----------------|----------------|--------------------|
| **Clareza e objetividade** | 30% | Mensagem direta, dentro do tempo, sem enrolação | Mensagem compreensível, tempo estourado ou subutilizado | Confusa ou muito fora do tempo |
| **Demonstração** | 30% | Mostra o produto/artefato funcionando, não slides sobre ele | Demonstração parcial | Só slides |
| **Evidência** | 25% | Afirmações sustentadas por dados do próprio projeto | Afirmações genéricas | Afirmações sem base |
| **Participação da equipe** | 15% | Todos os integrantes falam sobre o que fizeram | Maioria participa | Um só fala pelo grupo |

Nas apresentações, o docente pode dirigir perguntas a qualquer integrante sobre qualquer parte da entrega. A incapacidade de explicar a própria contribuição afeta o Fator de Participação individual.

---

## Checklist por sprint

Pode ser copiado para o `README.md` do repositório.

```markdown
### Sprint 0
- [ ] Repositório público + README completo
- [ ] docs/proposta.md (≤3 pág.)
- [ ] GitHub Projects com ≥10 itens, ≥3 estimados
- [ ] Coorte declarada (A=presencial / B=online)
- [ ] Integração com outra disciplina declarada (se houver)
- [ ] Vídeo 5 min

### Sprint 1
- [ ] Incremento funcional em main
- [ ] Kanban com WIP limits configurados
- [ ] Evidência de prática XP
- [ ] docs/retrospectiva-01.md com ações
- [ ] Vídeo 5 min

### Sprint 2
- [ ] CI verde (build + testes + lint) com gate em PR
- [ ] Dockerfile + docker-compose.yml
- [ ] docs/dora.md com as 5 métricas e método
- [ ] Segundo incremento
- [ ] Vídeo 5 min

### Sprint 3
- [ ] docs/vsm.md com tempos medidos
- [ ] ≥2 gargalos com dados
- [ ] 1–2 melhorias com métrica-alvo
- [ ] ≥3 PRs com revisão substantiva
- [ ] Evolução DORA S2→S3
- [ ] Vídeo 5 min

### Entrega Final
- [ ] MVP funcional, CI verde, README completo e licença
- [ ] docs/relatorio-final.md (≤6 pág.)
- [ ] docs/melhoria-de-processo.md (≤4 pág.)
- [ ] docs/topologia.md (≤1 pág.)
- [ ] docs/uso-de-ia.md
- [ ] Vídeo 10 min
- [ ] Apresentação ao vivo
```
