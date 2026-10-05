# Aula 05 - Agentes

Esta pasta contém a quinta versão do projeto da monitoria: uma aplicação Python que implementa um **agente capaz de decidir os próximos passos**, utilizando ferramentas quando necessário e repetindo o ciclo de decisão até conseguir produzir uma resposta final.

## O que muda na V5

Na Aula 04, aprendemos a expor ferramentas por meio de um servidor MCP e conectá-las a uma aplicação. Nesta aula, o foco passa a ser o comportamento de um **agente**.

Uma chamada comum com ferramentas funciona, de forma simplificada, assim:

> modelo solicita uma ferramenta → aplicação executa → resultado volta para o modelo → resposta

Um agente transforma esse processo em um **loop de decisão**:

> modelo decide → solicita ferramenta → aplicação executa → resultado volta ao modelo → modelo decide o próximo passo → ... → resposta final

Isso permite resolver tarefas em que uma ferramenta depende do resultado de outra.

Nesta aula, trabalhamos:

* diferença entre uma chamada com `tool` e um agente;
* execução de múltiplas ferramentas em sequência;
* ferramentas cujos resultados alimentam outras ferramentas;
* validação das ferramentas antes da execução;
* tratamento de erros sem interromper o agente;
* manutenção do histórico completo de mensagens durante o loop;
* limite máximo de iterações para evitar loops infinitos;
* registro dos passos para facilitar depuração e entendimento do comportamento do agente.

## Arquivos

- `aula5_agents_template.ipynb`: notebook com TODOs para a atividade;
- `env.example`: variáveis de ambiente esperadas;
- `requirements.txt`: dependências Python;
- `README.md`: este documento de configuração do ambiente.

**Nunca faça commit do arquivo `.env`.**