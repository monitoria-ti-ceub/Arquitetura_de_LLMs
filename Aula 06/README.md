# Aula 06 - RAG + Fechamento

Esta pasta contém a sexta versão do projeto da monitoria: uma aplicação Python que implementa **RAG (Retrieval-Augmented Generation)**, permitindo que o assistente consulte uma base de documentos antes de responder e utilize a busca como uma ferramenta dentro do agente.

## O que muda na V6

Na Aula 05, aprendemos a transformar chamadas de ferramentas em um **agente capaz de decidir os próximos passos**. Nesta aula, adicionamos uma base de documentos ao projeto e ensinamos o assistente a recuperar informações relevantes antes de responder.

O fluxo básico do RAG é:

> documentos → chunks → índice → busca → contexto recuperado → modelo → resposta

A aplicação divide os documentos em pequenos trechos, transforma esses trechos em vetores utilizando **TF-IDF** e recupera os trechos mais similares à pergunta por meio de **similaridade de cosseno**.

Depois, esses trechos são adicionados ao contexto enviado ao modelo, que recebe instruções para responder somente com base no material recuperado e citar suas fontes.

Nesta aula, trabalhamos:

* divisão de documentos em chunks com sobreposição;
* indexação dos chunks utilizando TF-IDF;
* busca por similaridade utilizando cosine similarity;
* construção de um prompt aumentado com o contexto recuperado;
* citação das fontes utilizadas na resposta;
* comportamento do assistente quando a informação não está na base;
* comparação entre respostas sem RAG e com RAG;
* transformação da busca de documentos em uma ferramenta do agente;
* integração entre RAG e o loop de decisão aprendido na Aula 05;
* fechamento da evolução do projeto desde a primeira versão.

## Arquivos

* `aula6_rag_template.ipynb`: notebook com TODOs para a atividade;
* `env.example`: variáveis de ambiente esperadas;
* `requirements.txt`: dependências Python;
* `README.md`: este documento de configuração do ambiente.

**Nunca faça commit do arquivo `.env`.**
