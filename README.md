# Artigo

As principais análises sobre o problema, implementação de código, referências e resultados encontram-se no artigo desse projeto. Disponível em: [Otimizando a Programação de Campeonatos de CS:GO: Uma Análise Estratégica de Redes de Competição Baseada em Teoria dos Grafos](./docs/Artigo-Otimizando-a-Programacao-de-Campeonatos-de-CSGO.pdf)

# Análise de Redes de Competição em Partidas Profissionais de CS:GO Utilizando Teoria dos Grafos

`Problema`: Utilizando a Teoria dos Grafos para Análise Estratégica de Rivalidades e Programação de Campeonatos em Partidas Profissionais de CS:GO.

## Construindo o Grafo

- `Vértices`: Cada equipe é representada como um vértice no grafo.

- `Arestas`: Uma aresta é estabelecida entre duas equipes (vértices) se elas disputaram uma partida entre si.

## Ponderando e Etiquetando as Arestas

- `Peso das Arestas`: O peso foi atribuído com base na frequência das partidas entre cada par de equipes. Por exemplo, se a equipe A jogou contra a equipe B em 10 partidas, a aresta entre A e B terá um peso maior em comparação com um par de equipes que jogou menos partidas entre si.

- `Etiquetas de Resultados`: Foram adicionadas informações sobre a contagem de vitórias/derrotas para cada par de equipes, o que ajudou a identificar rivalidades mais intensas.

- `Análise de Rank`: Posições no rank mundial na data da partida influenciam o limiar de rivalidade.

## Análise do Grafo

- `Determinando Rivalidades`: Uma alta frequência de confrontos (peso elevado nas arestas) indica uma rivalidade. Além disso, se os resultados desses confrontos forem equilibrados e a diferença do rank mundial de cada equipe, isso sugere uma rivalidade competitiva.

- `Conexões Frequentes`: Pares de equipes com um número significativo de partidas entre si serão evidentes pelo peso das arestas. Essas são as conexões mais frequentes.

## Visualização

A visualização do grafo ajuda a identificar rapidamente quais as conexões de uma equipe e quais são mais fortes.

### SK 2016

O time do SK Gaming esteve no top-1 no ano de 2016 e o resultado do grafo indica que sua maior rivalidade na época era o time da Dignitas, que na época era top-3.

<div align="justify">

![Alt text](./imgs/image-1.png)

![Alt text](./imgs/sk-top1-2016.png)

</div>

### SK 2017 - Ano mágico

O time do SK Gaming esteve no top-1 no ano de 2017 e foi o ano em que mais conquistou títulos. O resultado do grafo indica que sua maior rivalidade na época era o time da FaZe, que na época era top-2.

<div align="justify">

![Alt text](./imgs/image.png)

![Alt text](./imgs/sk-top1-2017.png)

</div>

Obs:. O rank mundial é muito volátil sendo atualizado toda semana. O limiar de rivalidade leva em consideração, para além da frequência das partidas, os resultados, o rank e também a evolução durante o período de tempo, então há de se considerar que nem sempre os times do topo vão apresentar maiores rivalidades.

## Algoritmo utilizado

Algoritmo de Força de Conexão (`Strength of Ties`):

Este algoritmo calcula a força das conexões (arestas) entre as equipes (vértices) com base na frequência das disputas, diferença do placar das partidas, diferença do rank das partidas e consistência da rivalidade através dos anos.

## Trabalhos Futuros

- `Contexto`: É importante considerar o contexto das partidas (como torneios importantes ou finais, rivalidade entre jogadores, rivalidade de torcidas) ao interpretar os resultados, pois eles podem adicionar uma camada adicional de significado às rivalidades identificadas.

Em resumo, a teoria dos grafos é uma ferramenta poderosa para analisar e visualizar as relações complexas e dinâmicas no cenário competitivo de Counter-Strike, permitindo identificar as maiores rivalidades e as conexões mais frequentes de forma eficaz.

## Extra

[**CS:GO - O JOGO QUE VALIA O TOP 1 DO MUNDO DE 2017!! (SK Vs FAZE) (ESL Pro League Season 6 Finals)**](https://www.youtube.com/watch?v=EjtxegacM_w)

<div align="justify">

![Alt text](./imgs/sk-faze-valendo-top1.png)

</div>
