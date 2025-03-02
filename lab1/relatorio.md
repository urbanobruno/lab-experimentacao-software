# Relatório
O Laboratório 1 consiste em coletar e analisar dados dos sistemas open-source mais populares do GitHub. A popularidade dos repositórios é calculada através do número de estrelas.


## Questões de Pesquisa
Para este laboratório temos que responder 6 perguntas através dos dados obtidos em virtude da nossa mineração. Elas são:

 - Sistemas populares são maduros/antigos?
 - Sistemas populares recebem muita contribuição externa?
 - Sistemas populares lançam releases com frequência?
 - Sistemas populares são atualizados com frequência?
 - Sistemas populares são escritos nas linguagens mais populares?
 - Sistemas populares possuem um alto percentual de issues fechadas?

## Métricas
Para cada pergunta existe uma métrica correspondente:

 - Idade do repositório;
 - Total de pull requests aceitas;
 - Total de releases;
 - Tempo até a última atualização;
 - Linguagem primária de cada repositório;
 - Razão entre número de issues fechadas pelo total de issues.

## Hipóteses Informais
Nesta seção, apresentaremos nossas hipóteses iniciais antes da coleta efetiva dos dados. Para cada pergunta, formulamos uma hipótese de resultados esperados.

 - Pergunta 1 - A maioria dos sistemas open-source mais populares são maduros/antigos.
 - Pergunta 2 - A maioria dos sistemas open-source recebe uma boa quantidade de contribuição externa.
 - Pergunta 3 - A maioria dos sistemas open-source não lançam mais muitos releases com frequência, por se tratarem de sistemas mais antigos/maduros.
 - Pergunta 4 - A maioria dos sistemas open-source recebem atualizações frequentemente.
 - Pergunta 5 - Não necessariamente os sistemas open-source são escritos nas linguagens mais populares. Principalmente pelo fato de acreditarmos que estamos tratando de sistemas mais antigos/maduros.
 - Pergunta 6 - Sim, sistemas open-source populares possuem um alto percentual de issues fechadas por possuírem um grande número de contribuição e serem sistemas mais antigos/maduros.

Com relação às métricas nossas hipóteses são:

 - Idade do repositório: Esperamos encontrar repositórios com idades entre 3 a 10 anos;
 - Total de pull requests aceitas: Esperamos encontrar mais pull requests aceitas do que em projetos fechados;
 - Total de releases: Acreditamos que o total de releases varia de acordo com a idade e características especificas dos repositórios;
 - Tempo até a última atualização: Esperamos encontrar algo entre 1 semana a 1 mês;
 - Linguagem primária de cada repositório: Esperamos encontrar linguagens mais consolidadas e robustas no mercado;
 - Razão entre número de issues fechadas pelo total de issues: acreditamos encontrar uma razão entre 60% a 80% de issues fechadas.

## Metodologia Utilizada

Para responder às perguntas, realizamos uma coleta de dados através de um algoritmo desenvolvido através da linguagem Python utilizando a API do GitHub para obter os dados dos repositórios. Após a coleta de dados, armazenamos os resultados em um arquivo CSV. A partir desse armazenamento realizamos a nossa análise, chegando às nossas conclusões.

## Resultados Obtidos

- Pergunta 1 - A idade média dos repositórios Open-source mais populares foi de 8.3 anos. Logo  podemos dizer que os sistemas Open-source mais populares são mais maduros/antigos.
- Pergunta 2 - A quantidade de pull requests (mediana) foi de 620. Não podemos concluir muita coisa pela quantidade de pull requests, mas é um forte indicador de que existe uma boa atenção externa para esses repositórios.
- Pergunta 3 - A quantidade de releases foi de 33 (mediana). Podemos concluir que os sistemas Open-source mais populares recebem uma grande quantidade de releases.
- Pergunta 4 - A frequência de atualizações da maioria dos sistemas Open-source mais populares foi de 6 dias (mediana). Logo, as atualizações são muito frequentes.
- Pergunta 5 - Sistemas Open-source populares possuem uma taxa de 86% de issues fechadas (mediana).
