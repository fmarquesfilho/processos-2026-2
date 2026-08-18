# Guia da Sprint 0 — DIM0510

Prazo em [CRONOGRAMA.md](CRONOGRAMA.md#visão-geral). O que entregar e como é avaliado: [RUBRICAS.md](RUBRICAS.md#sprint-0).

A Sprint 0 é a fase de planejamento: a equipe define o que vai construir e, principalmente, **como vai trabalhar**.

---

## Sobre o projeto desta disciplina

Neste projeto, **processo pesa tanto quanto o produto**. A equipe é avaliada sobretudo pela qualidade com que conduz o próprio processo de desenvolvimento.

**Stack tecnológico é livre.** O requisito é que o projeto permita demonstrar práticas de processo: integração contínua, testes, revisão de código, medição de fluxo.

Quem cursa também Web II ou Sistemas Móveis pode usar o **mesmo produto** nas duas disciplinas, com entregáveis distintos: aqui o foco é o processo — como a equipe trabalhou, métricas, retrospectiva — e lá é o produto. Isso dá direito ao bônus de integração descrito em [AVALIACAO.md](AVALIACAO.md#5-bônus-de-integração).

---

## Visão do produto

Declaração que responde por que o produto existe e qual problema resolve. Use este template:

```
Para [usuários-alvo]
Que [problema ou necessidade]
O [nome do produto] é um [categoria]
Que [benefício principal]
Diferente de [alternativa existente]
Nosso produto [diferencial único]
```

**Exemplo:**

```
Para estudantes que dividem apartamento
Que discutem no fim do mês quem pagou o quê
O Rateio é uma ferramenta de divisão de despesas
Que registra gastos e calcula quem deve a quem
Diferente de planilhas compartilhadas
Nosso produto fecha o mês com o menor número de transferências
```

Verifique se a visão define o usuário, nomeia um problema específico, explicita o valor único e é realista para um semestre com equipe de até quatro pessoas.

---

## Definição do MVP

O MVP é o escopo mínimo que entrega valor. Declare explicitamente o que fica **fora**.

**Exemplo, para o Rateio:**

| No MVP | Fora do MVP |
|---|---|
| Cadastro de grupo e participantes | Integração com bancos ou Pix |
| Registro de despesa com divisão | Aplicativo móvel |
| Cálculo do saldo de cada um | Divisão por porcentagem customizada |
| Fechamento de mês com sugestão de transferências | Histórico de meses anteriores |

Enuncie também a hipótese de valor: *acreditamos que [usuários] vão [comportamento] porque [benefício]*.

---

## Backlog e quadro Kanban

O backlog vive no **GitHub Projects**, em formato Kanban, com as colunas:

| Coluna | Significado |
|---|---|
| Backlog | Priorizado, mas fora da sprint atual |
| Sprint Backlog | Comprometido para a sprint corrente |
| Em progresso | Em desenvolvimento |
| Em revisão | Aguardando revisão de código |
| Pronto | Atende à Definição de Pronto |

Formato de história de usuário: **como [papel], quero [ação] para [benefício]**.

| Prio | História | Critérios de aceitação | Sprint |
|---|---|---|---|
| P1 | Como morador, quero registrar uma despesa para não esquecer | Valor, data, pagante e participantes; validação de valor positivo | 1 |
| P1 | Como morador, quero ver meu saldo para saber se devo ou tenho a receber | Saldo por pessoa; soma dos saldos igual a zero | 1 |
| P2 | Como grupo, queremos fechar o mês para zerar as contas | Sugere o menor conjunto de transferências | 2 |

P1 é essencial ao MVP, P2 é importante, P3 é desejável.

---

## Acordo de processo

Defina e registre:

- **Cadência**: duração da sprint, quando planejam e quando fecham
- **Cerimônias**: quais adotam, com que frequência e quanto tempo
- **Definição de Pronto**: o que precisa ser verdade para um item sair de "Em revisão"
- **Papéis**: quem faz o quê, incluindo quem revisa código de quem
- **Ferramentas**: onde conversam, onde registram decisões, onde medem
- **WIP limits**: quantos itens simultâneos por coluna

Este acordo será confrontado com a realidade nas sprints seguintes. Ele pode mudar — o que não pode é não existir.

---

## Estrutura do vídeo — 5 minutos

| Tempo | Conteúdo |
|---|---|
| 30 s | Equipe: nome, integrantes e papéis |
| 1 min 30 s | Visão do produto: problema, público e proposta de valor |
| 1 min 30 s | MVP: o que entra, o que fica fora, critérios de sucesso |
| 1 min 30 s | **Processo da equipe**: cadência, cerimônias, Definição de Pronto, quadro Kanban configurado e como vão colaborar |

Todos os integrantes devem falar. 

---

## Estrutura de `docs/proposta.md`

1. Visão do produto, no template
2. Definição do MVP: dentro e fora do escopo
3. Link para backlog inicial, com as histórias priorizadas (pode ser pro próprio repositório caso backlog esteja registrado nele, p. ex. GitHub Projects mora dentro do repositório do GitHub)
4. Stack tecnológico e justificativa
5. **Acordo de processo**: cadência, cerimônias, Definição de Pronto, ferramentas, WIP limits
6. Equipe: nome, matrícula e papel de cada integrante
7. Coorte de apresentação, link do quadro no GitHub Projects e, se houver, integração com outra disciplina

Máximo 3 páginas.
