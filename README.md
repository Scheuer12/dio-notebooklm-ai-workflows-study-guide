# NotebookLM Study Guide: AI Agents and Workflows

**Language:** The complete study guide is written in Portuguese.

This repository documents a DIO module project in which I used NotebookLM
to curate technical sources and organize practical notes on agent design,
explicit workflows, orchestration, guardrails, memory, observability, and
human approval.

It is a learning artifact, not an executable agent system. Its focus is the
documented study method: source selection, prompt iteration, lessons learned,
reusable prompts, and architecture checklists.

## Miniguia em português

Projeto de fim de modulo da DIO usando o NotebookLM como ferramenta de
aprendizagem ativa, curadoria de fontes e organizacao do conhecimento.

## 1. Contexto e objetivos

O tema escolhido para este caderno tematico foi:

> Como estruturar AI Agents e AI Companies: agentes especializados, ferramentas, workflows, guardrails, memoria, orquestracao e operacao continua.

Escolhi esse tema porque ele conecta inteligencia artificial aplicada, arquitetura de sistemas, automacao, produto, operacoes e tomada de decisao. A ideia nao e estudar IA generativa de forma generica, mas entender como transformar agentes em uma estrutura funcional: agentes com papeis claros, ferramentas adequadas, limites de autonomia, criterio de validacao e capacidade de evoluir com o tempo.

Neste projeto, o termo **AI Company** e usado como uma metafora pratica: uma organizacao composta por agentes especializados que trabalham como departamentos, squads ou funcoes de negocio. Cada agente precisa ter uma responsabilidade clara, entradas e saidas definidas, ferramentas, memoria, criterios de qualidade e pontos de escalonamento humano.

### Objetivos de aprendizagem

- Entender o que caracteriza um AI Agent na pratica.
- Diferenciar agente, workflow, ferramenta, automacao e multi-agent system.
- Estudar padroes de orquestracao como manager, handoffs e workflows explicitos.
- Compreender guardrails, validacao, memoria, observabilidade e limites de autonomia.
- Criar um miniguia para consultar rapidamente ao desenhar agentes e AI Companies.
- Documentar prompts reutilizaveis para tirar duvidas, revisar arquiteturas e manter o conhecimento atualizado.

## 2. Curadoria de fontes

Foram selecionadas fontes abertas, oficiais ou tecnicamente confiaveis, priorizando materiais recentes sobre agentes, orquestracao, workflows e uso do NotebookLM.

| Fonte | Tipo | Motivo da escolha |
| --- | --- | --- |
| [Google NotebookLM Help - Learn about NotebookLM](https://support.google.com/notebooklm/answer/16164461?hl=en) | Documentacao oficial | Explica como o NotebookLM funciona como assistente de pesquisa baseado em fontes. |
| [OpenAI Agents SDK - Agents](https://openai.github.io/openai-agents-python/agents/) | Documentacao oficial | Define agentes como LLMs com instrucoes, ferramentas, handoffs, guardrails e outputs estruturados. |
| [OpenAI Agents SDK - Guardrails](https://openai.github.io/openai-agents-python/guardrails/) | Documentacao oficial | Ajuda a entender validacao de entrada, saida e uso de ferramentas. |
| [Google Agent Development Kit - Get started](https://github.com/google/adk-docs/blob/main/docs/get-started/index.md) | Documentacao oficial/open source | Mostra a proposta de construir, gerenciar, avaliar e implantar agentes em diferentes linguagens. |
| [Microsoft Agent Framework - Overview](https://learn.microsoft.com/en-us/agent-framework/overview/) | Documentacao oficial | Traz uma distincao importante entre agentes e workflows e orienta quando usar cada abordagem. |
| [Microsoft AutoGen - Documentation](https://microsoft.github.io/autogen/dev/) | Documentacao tecnica | Referencia util para sistemas single-agent e multi-agent, com Core, AgentChat, Extensions e MCP. |

## 3. Metodo usado no NotebookLM

O processo de estudo foi dividido em cinco etapas:

1. Upload das fontes no NotebookLM.
2. Perguntas exploratorias para entender os conceitos centrais.
3. Perguntas comparativas para diferenciar agentes, workflows, ferramentas e empresas de agentes.
4. Perguntas aplicadas para desenhar uma AI Company funcional.
5. Consolidacao em um miniguia com resumo, glossario, prompts reutilizaveis e checklist de arquitetura.

O criterio principal foi estudar agentes como sistemas reais, nao como personagens de prompt. Um agente util precisa executar trabalho, lidar com contexto, chamar ferramentas, produzir saidas verificaveis e respeitar limites de autonomia.

## 4. Engenharia de prompts e cicatrizes

Esta etapa registra os prompts testados, as dificuldades encontradas e os ajustes feitos para melhorar a qualidade das respostas.

### Prompt 1 - Entendimento inicial

```text
Com base nas fontes selecionadas, explique o que e um AI Agent na pratica. Diferencie agente, chatbot, workflow, automacao e ferramenta.
```

Resultado observado:

- A resposta explicou bem os conceitos, mas ainda ficou muito abstrata.
- O NotebookLM trouxe definicoes corretas, mas pouco conectadas a arquitetura de sistemas.

Ajuste feito:

```text
Refaca a resposta como se eu fosse desenhar uma pequena empresa composta por agentes de IA. Para cada conceito, mostre: papel, exemplo, entrada, saida e risco principal.
```

Cicatriz:

Quando o tema e arquitetura de agentes, pedir apenas definicoes gera uma resposta limpa, mas pouco acionavel. Pedir entrada, saida e risco transforma o conteudo em material de projeto.

### Prompt 2 - Agente versus workflow

```text
Compare quando devo usar um agente autonomo e quando devo usar um workflow explicito. Use criterios praticos para tomada de decisao.
```

Resultado observado:

- A resposta trouxe uma boa diferenca entre tarefas abertas e processos bem definidos.
- Faltou uma matriz de decisao reutilizavel.

Ajuste feito:

```text
Transforme a comparacao em uma matriz com: tipo de tarefa, nivel de previsibilidade, autonomia necessaria, risco, exemplo e recomendacao de arquitetura.
```

Cicatriz:

Agentes sao atraentes, mas nem tudo deveria virar agente. Em tarefas previsiveis, workflows explicitos podem ser mais baratos, auditaveis e seguros.

### Prompt 3 - Estrutura de uma AI Company

```text
Desenhe uma AI Company simples composta por agentes especializados. Inclua agentes, responsabilidades, ferramentas, memoria, handoffs e pontos de intervencao humana.
```

Resultado observado:

- A primeira resposta criou muitos agentes.
- A estrutura ficou interessante, mas complexa demais para um MVP.

Ajuste feito:

```text
Reduza para uma versao MVP com no maximo 5 agentes. Cada agente deve ter uma responsabilidade clara, uma entrada principal, uma saida principal e um criterio de sucesso.
```

Cicatriz:

Multi-agent systems podem virar complexidade decorativa. Uma AI Company precisa comecar pequena, com agentes realmente necessarios.

### Prompt 4 - Guardrails e validacao

```text
Quais guardrails uma AI Company precisa para operar com seguranca? Considere entrada do usuario, saida do agente, chamada de ferramentas e decisoes que exigem aprovacao humana.
```

Resultado observado:

- A resposta trouxe riscos importantes, mas misturou politicas, validacoes tecnicas e boas praticas.

Ajuste feito:

```text
Organize os guardrails em quatro categorias: input, output, tool-use e human approval. Para cada uma, explique o que validar, quando bloquear e quando escalar para humano.
```

Cicatriz:

Guardrails precisam estar ligados a pontos especificos do fluxo. Falar "tenha seguranca" nao basta; e necessario dizer onde validar e o que acontece quando algo falha.

### Prompt 5 - Atualizacao continua

```text
Como posso usar este caderno no NotebookLM para me manter atualizado sobre AI Agents e tirar duvidas rapidamente em novos projetos?
```

Resultado observado:

- A resposta sugeriu revisoes periodicas, mas sem um processo concreto.

Ajuste feito:

```text
Crie um processo de manutencao do caderno com frequencia, tipos de fontes a adicionar, perguntas de revisao, criterios para substituir fontes antigas e formato de changelog.
```

Cicatriz:

Um caderno de estudo tecnico perde valor se nao houver manutencao. Para temas como AI Agents, a atualizacao precisa ser parte do sistema.

## 5. Miniguia de estudo

### 5.1 Ideia central

Um AI Agent nao e apenas um prompt com nome. Na pratica, um agente e um sistema que combina:

- um modelo de linguagem;
- instrucoes;
- contexto;
- ferramentas;
- memoria ou estado;
- criterios de validacao;
- comportamento de execucao;
- limites de autonomia;
- logs ou rastreabilidade.

Uma AI Company e uma organizacao de agentes com responsabilidades distribuidas. Ela pode conter agentes para pesquisa, analise, planejamento, execucao, revisao, atendimento, vendas, operacoes, desenvolvimento, qualidade e gestao.

### 5.2 Diferencas importantes

| Conceito | O que e | Quando usar |
| --- | --- | --- |
| Chatbot | Interface conversacional simples. | Perguntas e respostas com baixa autonomia. |
| Workflow | Sequencia explicita de passos. | Processos previsiveis, auditaveis e repetitivos. |
| Tool | Funcao ou servico chamado pelo agente. | Buscar dados, escrever arquivos, consultar APIs, executar tarefas. |
| AI Agent | Modelo com instrucoes, ferramentas e comportamento autonomo controlado. | Tarefas abertas, ambiguidade, decisao contextual e uso de ferramentas. |
| Multi-agent system | Conjunto de agentes especializados que colaboram. | Problemas grandes demais para um unico agente ou com competencias distintas. |
| AI Company | Metafora organizacional para agentes operando como uma empresa. | Estruturar agentes por funcoes de negocio, com governanca e operacao continua. |

### 5.3 Padroes de arquitetura

#### 1. Agente unico com ferramentas

Um agente central recebe a tarefa, decide quais ferramentas usar e retorna a resposta.

Uso ideal:

- MVPs;
- assistentes pessoais;
- tarefas com escopo moderado;
- baixa necessidade de especializacao.

Risco:

- agente acumula responsabilidades demais.

#### 2. Manager com agentes como ferramentas

Um agente orquestrador chama agentes especializados como se fossem ferramentas.

Uso ideal:

- sistemas com varias competencias;
- controle centralizado;
- consolidacao de respostas.

Risco:

- gargalo no orquestrador.

#### 3. Handoffs

Um agente transfere a conversa ou tarefa para outro agente especializado.

Uso ideal:

- atendimento;
- triagem;
- dominios com especialistas bem definidos.

Risco:

- perda de controle se os limites de transferencia nao forem claros.

#### 4. Workflow explicito

O fluxo e definido por etapas, condicoes e regras.

Uso ideal:

- processos repetitivos;
- tarefas com compliance;
- validacao forte;
- custos previsiveis.

Risco:

- pouca flexibilidade quando o problema muda.

### 5.4 Exemplo de AI Company MVP

| Agente | Responsabilidade | Entrada | Saida | Criterio de sucesso |
| --- | --- | --- | --- | --- |
| Orchestrator Agent | Entender a demanda, escolher fluxo e consolidar resultado. | Pedido do usuario. | Plano de execucao e resposta final. | Tarefa entregue com clareza e sem acao fora da autonomia permitida. |
| Research Agent | Buscar e sintetizar informacoes confiaveis. | Pergunta de pesquisa. | Resumo com fontes e grau de confianca. | Fontes relevantes e conclusoes separadas de inferencias. |
| Systems Designer Agent | Desenhar arquitetura, fluxos, schemas e integracoes. | Objetivo do sistema. | Proposta tecnica ou diagrama textual. | Solucao simples, modular e viavel. |
| Execution Agent | Criar artefatos, arquivos, scripts ou automacoes. | Plano aprovado. | Entregavel funcional. | Entrega testavel e aderente ao escopo. |
| QA / Guardrail Agent | Revisar qualidade, riscos, consistencia e seguranca. | Entregavel gerado. | Parecer de validacao e ajustes. | Problemas criticos identificados antes do uso real. |

### 5.5 Checklist para criar um agente

Antes de criar um agente, responder:

- Qual problema ele resolve?
- Esse problema exige agente ou um workflow resolveria melhor?
- Quais entradas ele recebe?
- Quais saidas ele deve produzir?
- Quais ferramentas ele pode usar?
- Que dados ele pode acessar?
- O que ele nao pode fazer?
- Quando deve pedir aprovacao humana?
- Como sua resposta sera validada?
- Como erros, incertezas e logs serao registrados?

### 5.6 Checklist para criar uma AI Company

Antes de criar varios agentes:

- Existe um orquestrador ou fluxo principal?
- Cada agente tem uma funcao diferente e necessaria?
- Existem contratos claros de comunicacao entre agentes?
- Os handoffs sao explicitos?
- Ha separacao entre pesquisa, decisao, execucao e revisao?
- Existem guardrails por entrada, saida e ferramentas?
- Ha registro de decisoes?
- O sistema pode ser depurado?
- E possivel comecar com menos agentes?

## 6. Glossario

| Termo | Definicao |
| --- | --- |
| AI Agent | Sistema baseado em LLM com instrucoes, ferramentas, contexto e comportamento orientado a tarefas. |
| Tool | Funcao, API, script ou servico que um agente pode chamar para executar uma acao. |
| Handoff | Transferencia de uma tarefa ou conversa de um agente para outro. |
| Orchestrator | Agente ou componente responsavel por coordenar fluxos e especialistas. |
| Guardrail | Validacao ou regra de seguranca aplicada a entrada, saida ou uso de ferramentas. |
| Workflow | Processo definido por etapas e regras explicitas. |
| Memory | Informacoes persistentes ou historico usados para manter contexto ao longo do tempo. |
| State | Estado atual de uma execucao, tarefa ou conversa. |
| MCP | Model Context Protocol, padrao para conectar modelos a ferramentas e fontes de contexto. |
| RAG | Retrieval-Augmented Generation, tecnica em que o modelo usa documentos recuperados como contexto. |
| Structured output | Saida em formato previsivel, como JSON aderente a schema. |
| Observability | Capacidade de rastrear execucao, chamadas, erros, custos e decisoes do sistema. |
| Human-in-the-loop | Ponto em que uma pessoa revisa, aprova ou corrige uma acao do agente. |

## 7. Prompts reutilizaveis

### Prompt para entender um conceito

```text
Com base nas fontes do caderno, explique [CONCEITO] no contexto de AI Agents. Separe: definicao, exemplo pratico, quando usar, quando nao usar e riscos.
```

### Prompt para desenhar um agente

```text
Desenhe um AI Agent para resolver [PROBLEMA]. Inclua: objetivo, entradas, saidas, ferramentas, memoria necessaria, limites de autonomia, guardrails, criterios de sucesso e riscos.
```

### Prompt para decidir entre agente e workflow

```text
Avalie se [TAREFA] deve ser resolvida com um AI Agent, um workflow explicito ou uma combinacao dos dois. Use criterios de previsibilidade, risco, custo, autonomia, auditabilidade e manutencao.
```

### Prompt para desenhar uma AI Company

```text
Proponha uma AI Company MVP para [OBJETIVO]. Limite a no maximo 5 agentes. Para cada agente, defina responsabilidade, entrada, saida, ferramentas, handoffs, guardrails e criterio de sucesso.
```

### Prompt para revisar arquitetura

```text
Revise a arquitetura abaixo como um arquiteto de AI Agents. Aponte excesso de complexidade, agentes desnecessarios, riscos, falhas de handoff, ausencia de guardrails, problemas de memoria e oportunidades de simplificacao.

Arquitetura:
[INSERIR ARQUITETURA]
```

### Prompt para atualizacao continua

```text
Com base nas fontes atuais e em novas fontes que eu adicionar, atualize meu resumo sobre AI Agents. Separe: novidades relevantes, conceitos que mudaram, praticas recomendadas, praticas obsoletas e impactos nos meus projetos.
```

## 8. Processo de manutencao do caderno

Para manter o caderno util ao longo do tempo:

- Revisar fontes a cada 15 ou 30 dias.
- Adicionar documentacoes oficiais antes de artigos opinativos.
- Registrar data de inclusao de cada fonte.
- Substituir fontes antigas quando houver mudanca relevante em SDKs, frameworks ou boas praticas.
- Manter um changelog com decisoes aprendidas.
- Usar prompts de revisao antes de aplicar conceitos em projetos reais.

## 9. Aprendizados finais

O principal aprendizado deste projeto foi que agentes de IA devem ser tratados como sistemas operacionais de trabalho, nao apenas como conversas inteligentes.

Um bom agente precisa ter papel, limite, ferramenta, memoria, validacao e criterio de sucesso. Uma boa AI Company precisa ter divisao de responsabilidades, orquestracao, governanca e capacidade de evolucao.

Tambem ficou claro que mais agentes nao significa melhor sistema. Muitas vezes, a melhor arquitetura e comecar com um unico agente bem definido, depois evoluir para workflows, handoffs e especialistas conforme a necessidade real aparecer.

## 10. Conclusao

Este caderno tematico mostrou como o NotebookLM pode apoiar estudo ativo em um tema tecnico emergente e em constante mudanca.

A partir das fontes selecionadas, foi possivel criar um miniguia pratico para consultar conceitos, revisar arquiteturas e tomar decisoes sobre AI Agents e AI Companies. A principal conclusao e simples: agentes bons nao nascem de prompts bonitos, mas de sistemas bem desenhados.

