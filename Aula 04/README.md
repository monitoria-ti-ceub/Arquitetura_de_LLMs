# Aula 04 - MCP e SDKs

Esta pasta contém a quarta versão do projeto da monitoria: uma aplicação Python que permite ao modelo solicitar a execução de ferramentas de um servidor MCP, assim como elucida o processo de criação/conexão de um.

## O que muda na V4

Na Aula 04, a aplicação selecionava ferramentas que ela iria utilizar, e solicitava a sua execução para geração de contexto, nesta nós abstraimos tudo que aprendemos em um único servidor, para que a solicitação não mais possa ser feita por somente uma aplicação:

- define o contrato de uso das ferramentas;
- cria um servidor mcp do zero;
- estabelece a conexão com a aplicação via client;
- faz uso das ferramentas quando necessário via algoritmo da IA

O servidor é local. A aula não depende de uma MCP externo.

## Arquivos

- `aula4_mcp_template.ipynb`: notebook com TODOs para a atividade;
- `env.example`: variáveis de ambiente esperadas;
- `requirements.txt`: dependências Python;
- `README.md`: este documento de configuração do ambiente.

**Nunca faça commit do arquivo `.env`.**
