# Plano de Curso — DIM0510 Processos de Software

**Curso**: Bacharelado em Engenharia de Software — UFRN/DIMAp
**Carga horária**: 60 horas
**Horário**: Segundas e quartas, 10:50 às 12:30 (24M56)
**Período**: 17/08/2026 a 19/12/2026
**Docente**: Fernando Figueira Filho — fernando.figueira@ufrn.br

As aulas de 10/08, 12/08 e 17/08 não foram realizadas. O curso inicia em 19/08.

---

## Ementa

Introdução a Processos de Software. Modelos de Ciclo de Vida de Software (cascata, espiral, modelo V, etc). Processos de Software existentes (processo unificado, metodologias ágeis). Modelagem e especificação de processos de software. Análise e medição de processos de software. Controle de qualidade em processos de software (revisões, inspeções, coleta e análise de métricas). Modelos de processos e padrões (IEEE, ISO). Implantação e Melhoria de Processos de Software.

---

## Objetivos

### Geral

Capacitar o estudante a compreender, analisar, projetar e melhorar processos de desenvolvimento de software, com ênfase em métodos ágeis, práticas DevOps e medição de desempenho de entrega.

### Específicos

Ao final do curso, o estudante será capaz de:

1. Comparar modelos de ciclo de vida clássicos e identificar seus contextos de aplicação
2. Aplicar Scrum, XP e Kanban em um projeto real com equipe
3. Projetar e operar pipelines de CI/CD com GitHub Actions e Docker
4. Medir desempenho de entrega com métricas DORA
5. Realizar Mapeamento de Fluxo de Valor (VSM) e identificar gargalos com dados
6. Aplicar controle de qualidade de processo: revisões, inspeções e métricas
7. Analisar organizações de equipe e princípios de Engenharia de Plataformas
8. Avaliar criticamente o impacto de ferramentas de IA em processos de software
9. Conduzir melhoria contínua com PDCA, kaizen e retrospectivas baseadas em dados
10. Relacionar modelos de maturidade e padrões (CMMI, ISO/IEC 12207, IEEE) às práticas modernas

---

## Organização do curso

O curso combina aulas presenciais expositivo-práticas com um projeto integrador desenvolvido em equipe ao longo do semestre.

### Estrutura das sprints

Uma Sprint 0 de quatro semanas, três sprints de projeto e um bloco final, com apresentações ao fim de cada sprint. Datas, conteúdo de cada aula e prazos: [CRONOGRAMA.md](CRONOGRAMA.md).


### Material de apoio

Serão divulgadas leituras e slides a cada início de sprint via SIGAA.

### Projeto integrador

Equipes de 1 a 4 estudantes desenvolvem um produto de software ao longo do semestre, aplicando em cada sprint os conceitos estudados. O repositório é público no GitHub e a atividade nele compõe a nota.

Equipes podem, opcionalmente, integrar este projeto com os de Web II (DIM0547) e Sistemas Móveis (DIM0524), com bônus na nota. Ver [AVALIACAO.md](AVALIACAO.md).

---

## Conteúdo programático

### Sprint 0 — Fundamentos e proposta

Introdução a processos de software. Modelos de ciclo de vida: cascata, espiral, modelo V, iterativo-incremental. Processo Unificado. Manifesto Ágil. Scrum: papéis, cerimônias e artefatos.

### Sprint 1 — Fluxo de trabalho

Extreme Programming: valores, práticas técnicas, design evolutivo, TDD, pair programming. Lean: sete princípios e sete desperdícios. Kanban: princípios, práticas, WIP limits, Lei de Little. Retrospectivas.

### Sprint 2 — Automação da entrega

Cultura DevOps: CALMS e os Três Caminhos. Integração e entrega contínuas com GitHub Actions. Containerização com Docker e Infrastructure as Code. Métricas DORA, framework SPACE e arquétipos de desempenho.

### Sprint 3 — Fluxo de valor e qualidade

Value Stream Mapping: estado atual, desperdício, lead time e cycle time, estado futuro. Controle de qualidade: revisões modernas de código, inspeções Fagan, critérios de aceite. Medição de processo. Modelos e padrões: ISO/IEC 12207, IEEE, CMMI V3.0.

### Bloco final — Organização, IA e consolidação

Melhoria contínua: PDCA, kaizen, implantação de processo e gestão da mudança. Governança de IA em processos. Adaptação de processos ao contexto. Apresentações finais. Topologias de Equipes: tipos de equipe, modos de interação, Lei de Conway. Engenharia de Plataformas. IA e processos de software: paradoxo da produtividade e DORA AI Capabilities Model.

---

## Avaliação

Nota final por média aritmética de três unidades, compostas pelas entregas das sprints e por duas provas escritas, valendo a maior das duas notas. Cada sprint é avaliada em entrega técnica, atividade no repositório e comunicação.

Composição, pesos e regras: [AVALIACAO.md](AVALIACAO.md). Critérios de cada entrega: [RUBRICAS.md](RUBRICAS.md).


---

## Ferramentas

| Ferramenta | Uso |
|------------|-----|
| GitHub | Repositório público do projeto e quadro Kanban (GitHub Projects) |
| GitHub Actions | Pipelines de CI/CD e coleta de métricas |
| Docker | Containerização |
| Multiprova | Provas escritas |
| Google Meet | Encontros online e apresentações remotas |
| Discord | Comunicação da turma |
| SIGAA | Entregas oficiais e notas |

O repositório do projeto deve permanecer público durante todo o semestre.

---

## Ambientes de desenvolvimento online

O stack é livre, e nenhuma etapa exige máquina própria com Docker instalado.

| Ambiente | Cadastro | O que roda | Limite |
|---|---|---|---|
| **GitHub Codespaces** | sim | VS Code no navegador, qualquer stack, Docker, testes, CI | 180 h por mês com o GitHub Student Pack |
| **Google Cloud Shell Editor** | conta Google | Linguagens comuns, Docker, 5 GB persistentes | CPU modesta; sessão expira por inatividade |

Vale notar a conexão com o conteúdo: um `.devcontainer/devcontainer.json` versionado é um artefato de processo. Ele torna o ambiente reproduzível para toda a equipe e para quem chegar depois — exatamente o argumento da Sprint 2 sobre containerização e Infrastructure as Code. Equipes que adotarem isso têm material pronto para a discussão de carga cognitiva e plataforma no bloco final.

---

## Bibliografia

### Básica

VALENTE, Marco Tulio. *Engenharia de Software Moderna*. UFMG, 2020. Disponível em: https://engsoftmoderna.info/

LETAW, Lara. *Handbook of Software Engineering Methods*. 2. ed. Oregon State University, 2024. Disponível em: https://open.oregonstate.education/setextbook/

IEEE COMPUTER SOCIETY. *SWEBOK Guide V4.0*. 2024. Disponível em: https://www.computer.org/education/bodies-of-knowledge/software-engineering/v4

### Complementar

BEYER, Betsy et al. *Site Reliability Engineering*. Google/O'Reilly, 2017. Disponível em: https://sre.google/sre-book/table-of-contents/

SCHWABER, Ken; SUTHERLAND, Jeff. *Guia do Scrum 2020*. Disponível em: https://scrumguides.org/

DORA TEAM. *Accelerate State of DevOps Report*. Google Cloud. Disponível em: https://dora.dev/

FOWLER, Martin. *Continuous Integration*; *Is Design Dead?* Disponível em: https://martinfowler.com/

GOOGLE. *Code Review Developer Guide*. Disponível em: https://google.github.io/eng-practices/review/

IEEE/ISO/IEC 12207:2017 — Software Life Cycle Processes. CMMI V3.0.

Toda a bibliografia é de acesso gratuito.
