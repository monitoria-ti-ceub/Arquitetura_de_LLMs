# Aula 03 - Tool Calling

Esta pasta contém a terceira versão do projeto da monitoria: uma aplicação Python que permite ao modelo solicitar a execução de funções externas.

## O que muda na V3

Na Aula 02, a aplicação selecionava contexto para o modelo ler. Agora ela também descreve ferramentas que o modelo pode solicitar:

- define o contrato de uma ferramenta com schema;
- envia as ferramentas junto com a requisição;
- inspeciona um `tool_call` retornado pelo modelo;
- executa uma função Python na aplicação;
- devolve o resultado em uma mensagem `tool`;
- faz uma nova chamada para o modelo produzir a resposta final.

As ferramentas são locais e determinísticas para que o fluxo fique visível. A aula não depende de uma API externa de calendário ou banco de dados.

## Arquivos

- `aula3_tool_calling_template.ipynb`: notebook com TODOs para a atividade;
- `env.example`: variáveis de ambiente esperadas;
- `requirements.txt`: dependências Python;
- `README.md`: este documento de configuração do ambiente.

**Nunca faça commit do arquivo `.env`.**
