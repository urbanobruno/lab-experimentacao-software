# Caracterização da Atividade de Code Review no GitHub

Este projeto foi desenvolvido como parte do trabalho da disciplina **Laboratório de Experimentação de Software**.

## Integrantes
- Bruno Rocha Corrêa Urbano
- Henrique Dani Franco Nezio
- Pedro de Barros Alves

## Objetivo

Este projeto tem como objetivo investigar fatores que influenciam o processo de code review em repositórios populares do GitHub, analisando Pull Requests (PRs) submetidos a esses projetos.

O estudo busca entender como características como tamanho, tempo de análise, qualidade da descrição e número de interações impactam o desfecho das PRs e o número de revisões realizadas.

## Questões de Pesquisa

Nosso estudo busca responder às seguintes questões:

- **RQ01:** Qual a relação entre o tamanho dos PRs e o feedback final das revisões?
- **RQ02:** Qual a relação entre o tempo de análise dos PRs e o feedback final das revisões?
- **RQ03:** Qual a relação entre a descrição dos PRs e o feedback final das revisões?
- **RQ04:** Qual a relação entre as interações nos PRs e o feedback final das revisões?
- **RQ05:** Qual a relação entre o tamanho dos PRs e o número de revisões realizadas?
- **RQ06:** Qual a relação entre o tempo de análise dos PRs e o número de revisões realizadas?
- **RQ07:** Qual a relação entre a descrição dos PRs e o número de revisões realizadas?
- **RQ08:** Qual a relação entre as interações nos PRs e o número de revisões realizadas?

## Metodologia

### Coleta de Dados

- Utilizamos a API GraphQL do GitHub para coletar informações sobre os 300 repositórios mais populares, baseados no número de estrelas.
- Selecionamos apenas repositórios que possuem pelo menos 100 Pull Requests fechadas (MERGED + CLOSED).
- Utilizando a API REST do GitHub, foram coletadas as Pull Requests de cada repositório filtrado, respeitando os seguintes critérios:
  - PRs com status Merged ou Closed.
  - PRs abertas por mais de uma hora (para excluir revisões automáticas ou muito rápidas).
  - PRs com pelo menos uma revisão formal realizada por revisores humanos.

### Extração de Métricas

Para cada Pull Request coletada, extraímos:
- Tempo de Análise: Horas entre a criação e o fechamento/merge da PR.
- Tamanho: Número de arquivos modificados, adições e remoções de linhas de código.
- Descrição: Número de caracteres no corpo (body) da PR.
- Interações: Número de participantes únicos, comentários gerais e comentários de revisão.
- Outras Informações: Estado final da PR (merged ou closed), autor da PR e tamanho do título.

### Tratamento e Visualização dos Dados

- As informações extraídas foram organizadas em um único conjunto de dados tabular (.csv).
- Foram utilizados valores medianos para sumarizar as métricas das PRs.
- A análise buscou encontrar correlações e padrões entre as variáveis coletadas e as questões de pesquisa propostas.

## Tecnologias Utilizadas

- **Python**: Linguagem principal para análise dos dados.
- **Google Colab**: Ambiente de desenvolvimento colaborativo.
- **API GraphQL do GitHub**: Coleta de dados dos repositórios.
- **API REST do GitHub**: Coleta detalhada das informações de Pull Requests.
- **Pandas**: Manipulação e análise de dados.
- **Requests** e **gql**: Bibliotecas para comunicação com a API do GitHub.
- **tqdm**: Barra de progresso para loops de coleta de dados.
