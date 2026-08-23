# Miniguia de Estudo

## Ideia central

Um AI Agent nao e apenas um prompt. E um sistema com instrucoes, ferramentas, contexto, estado, validacao e limites de autonomia.

Uma AI Company e uma organizacao de agentes especializados trabalhando em conjunto para executar funcoes de negocio, produto, operacoes ou tecnologia.

## Resumo rapido

- Chatbot responde conversas.
- Workflow segue passos definidos.
- Tool executa uma acao especifica.
- Agent decide como usar contexto e ferramentas para cumprir uma tarefa.
- Multi-agent system coordena agentes especializados.
- AI Company organiza agentes como funcoes de uma empresa.

## Checklist de arquitetura

Antes de criar um agente:

- Qual problema ele resolve?
- Ele precisa ser agente ou workflow basta?
- Quais entradas recebe?
- Quais saidas entrega?
- Quais ferramentas usa?
- Qual memoria precisa?
- Quais limites de autonomia possui?
- Quando deve escalar para humano?
- Como a qualidade sera validada?
- Como erros e decisoes serao registrados?

## AI Company MVP

Uma estrutura inicial pode conter:

- Orchestrator Agent;
- Research Agent;
- Systems Designer Agent;
- Execution Agent;
- QA / Guardrail Agent.

Essa estrutura cobre entendimento, pesquisa, desenho, execucao e revisao sem criar complexidade excessiva.

## Prompts reutilizaveis

```text
Desenhe um AI Agent para resolver [PROBLEMA]. Inclua: objetivo, entradas, saidas, ferramentas, memoria necessaria, limites de autonomia, guardrails, criterios de sucesso e riscos.
```

```text
Avalie se [TAREFA] deve ser resolvida com um AI Agent, um workflow explicito ou uma combinacao dos dois. Use criterios de previsibilidade, risco, custo, autonomia, auditabilidade e manutencao.
```

```text
Proponha uma AI Company MVP para [OBJETIVO]. Limite a no maximo 5 agentes. Para cada agente, defina responsabilidade, entrada, saida, ferramentas, handoffs, guardrails e criterio de sucesso.
```

```text
Revise a arquitetura abaixo como um arquiteto de AI Agents. Aponte excesso de complexidade, agentes desnecessarios, riscos, falhas de handoff, ausencia de guardrails, problemas de memoria e oportunidades de simplificacao.
```

