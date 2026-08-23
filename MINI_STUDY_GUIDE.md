# Miniguia de Estudo

## Ideia central

IA generativa fica mais util quando e usada com fontes confiaveis, prompts bem estruturados e criterios de validacao.

Em automacao de processos, o maior valor nao esta apenas em gerar textos, mas em transformar informacoes confusas em estruturas que podem ser analisadas, revisadas e reutilizadas.

## Resumo rapido

- NotebookLM ajuda a estudar com base em fontes selecionadas.
- Prompt engineering melhora clareza, foco e formato das respostas.
- Saidas estruturadas, como JSON, ajudam a conectar IA com sistemas e automacoes.
- Riscos como alucinacao, privacidade e erro operacional precisam ser tratados.
- Validacao humana e regras deterministicas continuam importantes.

## Checklist de uso pratico

Antes de usar IA em um processo:

- Existe uma fonte confiavel?
- O objetivo do prompt esta claro?
- O formato esperado da resposta foi definido?
- Existem exemplos?
- Ha campos obrigatorios?
- O que deve ser validado por uma pessoa?
- O que deve ser regra deterministica em vez de IA?
- As incertezas foram registradas?

## Prompts reutilizaveis

```text
Transforme a descricao abaixo em uma estrutura organizada. Separe fatos extraidos, inferencias, incertezas e perguntas de validacao.
```

```text
Converta as informacoes abaixo em JSON. Use apenas informacoes presentes no texto. Quando algo nao estiver claro, preencha o campo "uncertainties". Nao invente dados.
```

```text
Revise a resposta anterior como se ela fosse usada em um processo real. Aponte riscos, possiveis alucinacoes, campos sem evidencia, informacoes que precisam de validacao humana e melhorias no formato de saida.
```

