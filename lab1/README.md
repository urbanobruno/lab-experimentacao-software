# Análise de Repositórios Populares do GitHub

Este projeto faz parte do trabalho da disciplina de **Laboratório de Experimentação de Software**.

## Integrantes

- Bruno Rocha Corrêa Urbano
- Henrique Dani Franco Nezio
- Pedro de Barros Alves

## Objetivo
Este projeto tem como objetivo analisar características de 1.000 repositórios populares do GitHub. Por meio da API GraphQL do GitHub, coletamos diversas métricas para responder a questões de pesquisa relacionadas à maturidade, contribuição externa, frequência de releases, atualizações e uso de linguagens de programação.

## Questões de pesquisas

Nosso estudo busca responder as seguintes questões:

1. Sistemas populares são maduros/antigos?
   Métrica: Idade do repositório (calculada a partir da data de criação).

2. Sistemas populares recebem muita contribuição externa?
   Métrica: Total de pull requests aceitas.

3. Sistemas populares lançam releases com frequência?
   Métrica: Total de releases.

4. Sistemas populares são atualizados com frequência?
   Métrica: Tempo até a última atualização.

5. Sistemas populares são escritos nas linguagens mais populares?
   Métrica: Linguagem primária de cada repositório.

6. Sistemas populares possuem um alto percentual de issues fechadas?
   Métrica: Razão entre número de issues fechadas e total de issues.

7. Sistemas escritos em linguagens mais populares recebem mais contribuição externa, lançam mais releases e são atualizados com mais frequência?

## Metodologia
1. Coleta de Dados
- Utilizamos a API GraphQL do GitHub para buscar os 1.000 repositórios com maior número de estrelas.
- Extraímos informações básicas como nome, dono, data de criação, última atualização, linguagem primária e total de pull requests aceitas.

2. Refinamento dos Dados
- Para cada repositório, coletamos informações adicionais, como total de releases, total de issues abertas e fechadas.
- Armazenamos os dados em um arquivo .csv para análise posterior.

3. Análise e Visualização dos Dados
- Calculamos valores medianos para cada uma das métricas.
- Realizamos comparações entre diferentes linguagens.
- Elaboramos um relatório final com nossas hipóteses e a discussão dos resultados.

## Tecnologias Utilizadas

- **Python**: Linguagem principal para a coleta e análise dos dados.
- **Google Colab**: Plataforma utilizada para desenvolvimento colaborativo.
- **API GraphQL do GitHub**: Fonte dos dados analisados.
- **Pandas**: Biblioteca para manipulação e análise de dados.
- **Requests e gql**: Bibliotecas para fazer requisições e consultas GraphQL.

## Como Executar o Código

1. Clone este repositório.
2. Instale as dependências:

```bash
   pip install requests pandas gql
```
3. Substitua GITHUB_TOKEN no código pelo seu token pessoal do GitHub.
4. Execute o script principal em um ambiente Python ou Google Colab.

## Resultados e Discussão

As hipóteses formuladas pelo grupo e resultados obtidos estão apresentados no relatório final presente no arquivo **relatorio.md**, onde estão presentes comparações das nossas expectativas iniciais com os valores coletados, buscando responder as questões de pesquisa propostas.


