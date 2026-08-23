# Prompts e Cicatrizes

Este arquivo registra a engenharia de prompts usada no projeto e os ajustes feitos para melhorar as respostas.

## Prompt 1

```text
Com base nas fontes selecionadas, explique em linguagem simples como o NotebookLM pode ser usado para estudar IA aplicada a automacao de processos. Organize a resposta em: conceitos principais, aplicacoes praticas e cuidados.
```

Problema encontrado:

- Resposta clara, mas generica.
- Pouca conexao com automacao real.

Prompt ajustado:

```text
Agora aprofunde a resposta com foco em uso pratico: considere um profissional que precisa transformar descricoes confusas de processos em fluxos, dados estruturados e decisoes operacionais. Use exemplos concretos.
```

Aprendizado:

- Contexto de uso melhora a utilidade da resposta.

## Prompt 2

```text
Compare prompt engineering tradicional com o uso de saidas estruturadas, como JSON aderente a schema. Explique quando cada abordagem e suficiente e quando ela passa a ser limitada.
```

Problema encontrado:

- Resposta boa, mas pouco revisavel.

Prompt ajustado:

```text
Inclua uma tabela comparando: uso ideal, risco principal, exemplo pratico e como validar o resultado.
```

Aprendizado:

- Formatos tabulares ajudam a transformar explicacao em material de estudo.

## Prompt 3

```text
Imagine que um usuario descreve por voz um processo operacional confuso. Com base nas fontes, proponha um fluxo de IA para transformar essa descricao em dados estruturados, analise preliminar e proximos passos.
```

Problema encontrado:

- O fluxo pulava validacoes importantes.

Prompt ajustado:

```text
Refaca o fluxo incluindo pontos de validacao humana, checagem de campos obrigatorios, tratamento de incertezas e separacao entre fatos extraidos e inferencias da IA.
```

Aprendizado:

- Em processos reais, resposta bonita nao basta. Validacao e incerteza precisam aparecer.

## Prompt 4

```text
Usando as fontes sobre risco e boas praticas, liste os principais riscos de usar IA generativa em automacao de processos e proponha mitigacoes praticas.
```

Problema encontrado:

- Riscos apareceram de forma correta, mas abstrata.

Prompt ajustado:

```text
Reorganize os riscos em uma tabela operacional com: risco, exemplo em processo real, impacto possivel e mitigacao pratica.
```

Aprendizado:

- Para risco, tabela operacional e melhor que explicacao solta.

