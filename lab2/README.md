# Análise da Qualidade de Repositórios Java Populares do GitHub

Este projeto foi desenvolvido como parte do trabalho da disciplina **Laboratório de Experimentação de Software**.

## Integrantes
- Bruno Rocha Corrêa Urbano
- Henrique Dani Franco Nezio
- Pedro de Barros Alves

## Objetivo

Este projeto tem como objetivo investigar como diferentes características do processo de desenvolvimento — como **popularidade**, **maturidade**, **atividade** e **tamanho** dos repositórios — podem estar relacionadas com atributos de **qualidade interna do código-fonte**.  

Para isso, foram analisados **1.000 repositórios Java populares do GitHub**, utilizando a **API GraphQL** para coleta de dados de processo e a ferramenta **CK** para extração de métricas de qualidade de software.

## Questões de Pesquisa

Nosso estudo busca responder às seguintes questões:

- **RQ01:** Qual a relação entre a popularidade dos repositórios e suas características de qualidade?
- **RQ02:** Qual a relação entre a maturidade dos repositórios e suas características de qualidade?
- **RQ03:** Qual a relação entre a atividade dos repositórios e suas características de qualidade?
- **RQ04:** Qual a relação entre o tamanho dos repositórios e suas características de qualidade?

## Metodologia

### Coleta de Dados

- Utilizamos a **API GraphQL do GitHub** para buscar os **1.000 repositórios com maior número de estrelas** escritos em **Java**.
- Coletamos as seguintes métricas de processo:
  - **Popularidade:** número de estrelas
  - **Maturidade:** idade do repositório (em anos)
  - **Atividade:** número de releases
  - **Tamanho:** número de linhas de código e comentários (LOC)

### Análise de Qualidade

- Foi utilizada a ferramenta **[CK (Chidamber and Kemerer metrics)](https://github.com/mauricioaniche/ck)** para realizar análise estática dos repositórios e extrair as seguintes métricas:
  - **CBO (Coupling Between Objects)**
  - **DIT (Depth of Inheritance Tree)**
  - **LCOM (Lack of Cohesion of Methods)**

### Tratamento e Visualização dos Dados

- Os dados foram organizados e analisados utilizando **Python**, com auxílio das bibliotecas `Pandas`, `Matplotlib` e `Seaborn`.
- Os valores de cada métrica foram **sumarizados por repositório** (média, mediana e desvio padrão).
- A análise buscou encontrar correlações e padrões entre os indicadores de processo e as métricas de qualidade.

## Tecnologias Utilizadas

- **Python**: Linguagem principal para análise dos dados.
- **Google Colab**: Ambiente de desenvolvimento colaborativo.
- **API GraphQL do GitHub**: Coleta de dados dos repositórios.
- **CK**: Ferramenta para análise estática de código Java.
- **Pandas**: Manipulação e análise de dados.
- **Requests** e **gql**: Bibliotecas para comunicação com a API do GitHub.
