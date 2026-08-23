# Prompts e Cicatrizes

Este arquivo registra a engenharia de prompts usada no projeto e os ajustes feitos para melhorar as respostas no NotebookLM.

## Prompt 1 - Conceitos iniciais

```text
Com base nas fontes selecionadas, explique o que e um AI Agent na pratica. Diferencie agente, chatbot, workflow, automacao e ferramenta.
```

Problema encontrado:

- A resposta explicou conceitos, mas ainda ficou abstrata.

Prompt ajustado:

```text
Refaca a resposta como se eu fosse desenhar uma pequena empresa composta por agentes de IA. Para cada conceito, mostre: papel, exemplo, entrada, saida e risco principal.
```

Aprendizado:

- Para estudar arquitetura, exemplos com entrada, saida e risco funcionam melhor do que definicoes soltas.

## Prompt 2 - Agente versus workflow

```text
Compare quando devo usar um agente autonomo e quando devo usar um workflow explicito. Use criterios praticos para tomada de decisao.
```

Problema encontrado:

- A resposta foi boa, mas nao estava facil de aplicar em projetos.

Prompt ajustado:

```text
Transforme a comparacao em uma matriz com: tipo de tarefa, nivel de previsibilidade, autonomia necessaria, risco, exemplo e recomendacao de arquitetura.
```

Aprendizado:

- Nem toda tarefa precisa virar agente. Workflows explicitos podem ser melhores para processos previsiveis.

## Prompt 3 - AI Company MVP

```text
Desenhe uma AI Company simples composta por agentes especializados. Inclua agentes, responsabilidades, ferramentas, memoria, handoffs e pontos de intervencao humana.
```

Problema encontrado:

- A primeira versao criou agentes demais.

Prompt ajustado:

```text
Reduza para uma versao MVP com no maximo 5 agentes. Cada agente deve ter uma responsabilidade clara, uma entrada principal, uma saida principal e um criterio de sucesso.
```

Aprendizado:

- Multi-agent system sem necessidade real vira complexidade decorativa.

## Prompt 4 - Guardrails

```text
Quais guardrails uma AI Company precisa para operar com seguranca? Considere entrada do usuario, saida do agente, chamada de ferramentas e decisoes que exigem aprovacao humana.
```

Problema encontrado:

- A resposta misturou politicas, validacoes tecnicas e boas praticas.

Prompt ajustado:

```text
Organize os guardrails em quatro categorias: input, output, tool-use e human approval. Para cada uma, explique o que validar, quando bloquear e quando escalar para humano.
```

Aprendizado:

- Guardrails precisam estar ligados a pontos concretos do fluxo.

## Prompt 5 - Atualizacao continua

```text
Como posso usar este caderno no NotebookLM para me manter atualizado sobre AI Agents e tirar duvidas rapidamente em novos projetos?
```

Problema encontrado:

- A resposta sugeriu revisoes, mas sem processo claro.

Prompt ajustado:

```text
Crie um processo de manutencao do caderno com frequencia, tipos de fontes a adicionar, perguntas de revisao, criterios para substituir fontes antigas e formato de changelog.
```

Aprendizado:

- Um caderno tecnico precisa de manutencao, especialmente em temas que mudam rapido.

