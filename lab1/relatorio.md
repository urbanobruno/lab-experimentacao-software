# Relatório
O Laboratório 1 consiste em coletar e analisar dados dos sistemas open-source mais populares do GitHub. A popularidade dos repositórios é calculada através do número de estrelas.


## Questões de Pesquisa
Para este laboratório temos que responder 7 perguntas através dos dados obtidos em virtude da nossa mineração. Elas são:

 - Sistemas populares são maduros/antigos?
 - Sistemas populares recebem muita contribuição externa?
 - Sistemas populares lançam releases com frequência?
 - Sistemas populares são atualizados com frequência?
 - Sistemas populares são escritos nas linguagens mais populares?
 - Sistemas populares possuem um alto percentual de issues fechadas?
 - Sistemas escritos em linguagens mais populares recebem mais contribuição externa, lançam mais releases e são atualizados com mais frequência?

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
 - Pergunta 7 - Sim, sistemas escritos em linguagens mais populares recebem mais contribuições externas por possuírem uma base de desenvolvedores maior e uma comunidade mais ativa. Além disso, esses sistemas lançam mais releases, pois linguagens populares geralmente são utilizadas em projetos dinâmicos que exigem atualizações constantes. Da mesma forma, esses sistemas são atualizados com mais frequência já que contam com uma manutenção contínua devido à grande quantidade de usuários e contribuidores.

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
- Pergunta 5 - A análise revelou que Python, TypeScript e JavaScript dominam o cenário. Essas linguagens aparecem com uma quantidade significativamente maior de repositórios em comparação com outras, como Go, Java, C++ e Rust. Logo, isso indica que as linguagens mais populares no mercado também estão sendo bastante utilizadas nos repositórios open-source de maior popularidade.
- Pergunta 6 - Sistemas Open-source populares possuem uma taxa de 86% de issues fechadas (mediana).
- Pergunta 7 - Quanto à contribuição externa, linguagens como Rust, TypeScript e Go apresentaram as maiores medianas de pull requests aceitos. Já linguagens como C e HTML tiveram um número significativamente menor de contribuições aceitas. Quanto à frequência de releases, linguagens como TypeScript, Go e Rust tiveram as maiores medianas de releases. Já HTML e Shell apresentaram uma mediana muito baixa. Quanto à frequência de atualização, a mediana dos dias desde a última atualização foi praticamente idêntica para todas as linguagens analisadas.

## Discussão
- Pergunta 1 - O resultado confirma nossa hipótese de que sistemas populares tendem a ser mais maduros. A idade média de 8.3 anos está dentro do intervalo esperado (3 a 10 anos).
- Pergunta 2 - O resultado obtido é um forte indicativo de que os repositórios populares recebem contribuição externa, mas, de forma isolada, não permite uma conclusão definitiva. Embora o número seja significativo, ele pode variar conforme o tamanho e a natureza do projeto. No entanto, a tendência geral aponta que os sistemas mais populares são amplamente colaborativos.
- Pergunta 3 - O resultado obtido contradiz a nossa hipótese inicial. A quantidade de releases observada sugere que esses sistemas continuam a receber melhorias e novas versões regularmente. Assim, isso pode indicar que a popularidade está relacionada com uma gestão ativa do projeto, com atualizações e manutenção frequentes.
- Pergunta 4 - O resultado confirma nossa hipótese de que sistemas populares são frequentemente atualizados. A média de 6 dias está dentro do intervalo esperado e indica um alto nível de manutenção e evolução nos projetos analisados. Portanto, entendemos que isso pode ser um fator determinante para a popularidade e longevidade dos repositórios.
- Pergunta 5 - Os dados obtidos mostraram que as linguagens mais populares atualmente, como Python, TypeScript e JavaScript, dominam o cenário dos repositórios open-source populares. Assim, os resultados contradizem nossa hipótese inicial, pois mostram que há uma forte relação entre as linguagens mais utilizadas no mercado e as dos sistemas open-source mais populares.
- Pergunta 6 - O resultado confirma nossa hipótese e ainda a supera. A taxa de 86% indica que os repositórios populares possuem uma gestão eficiente de issues, provavelmente devido ao alto nível de contribuição externa e envolvimento da comunidade.
- Pergunta 7 - Quanto à contribuição externa, os resultados obtidos indicam que sistemas escritos em linguagens mais populares tendem a receber mais contribuições externas, assim confirmando a nossa hipótese inicial. Isso sugere que a popularidade da linguagem pode ser um fator influente no nível de engajamento da comunidade. Quanto à frequência de releases, os resultados obtidos mostraram pouca variação entre as linguagens analisadas, assim contradizendo parcialmente a nossa hipótese inicial. Isso pode indicar que, independentemente da linguagem utilizada, os projetos seguem um ritmo semelhante de manutenção e evolução contínua. Quanto à frequência de atualização, os resultados obtidos indicam que sistemas escritos em linguagens mais populares lançam novas versões de forma praticamente idêntica, não havendo muitas alterações entre as linguagens analisadas, assim contradizendo parcialmente a nossa hipótese inicial, pois não há uma variação evidente que sustente a nossa hipótese.


