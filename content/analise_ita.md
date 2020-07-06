---
title: "O Quadrilátero Ferrífero tem mais casos confirmados, proporcionalmente, do que o resto de Minas Gerais?"
date: 2020-06-14T23:35:27-03:00
draft: false
images:
  - https://picsum.photos/1024/768/?random
---Hipotese:
A quantidade de obitos confirmados por coronavírus em itabira seguem mesma distribuição que a letalidade no Quadrilátero Ferrífero.

Teste:
É possivel verificar se conseguimos descrever quantas casos evoluiram para óbito, utilizando a letalidade do Quadrilátero Ferrífero sem a microrregião de Itabira.
A população da Microrregião foi subtraida da população do quadrilátero para não contaminar os dados, tornando-os enviesados.

X ~ Binomial(n,p)

X = 2 -- Número de obitos de Corona vírus na Microrregião de Itabira.

n = 1095 -- Número da população que testou positivo para coronavírus na Microrregião de Itabira

p = 0.021 -- probabilidade de sucesso (letalidade no Quadrilátero sem a microrregião de Itabira)

X ~ Binomial(1095, 0.021)

mean = 23

SD = 4.74

Grafico probabilidades de evento:
![normal](/grafico_site_itabira.jpg)

(Quantidade de óbitos dada a população X probabilidade do evento ocorrer.)

Óbitos registrados: 2
z = -4.42

fdp - P(X=2) = 2.22e-08
fdp - P(X >=2) = 0.999

Hipótese nula = a probabilidade de sucesso de 0.021 descreve a distribuição do Quadrilátero Ferrífero.
Hipótese alternativa = a probabilidade de sucesso verdadeira não é 0.021

p-valor = 4.06e-08
p-valor < 0.05 (Hipotese nula negada)

Conclusão:
É improvavel que o evento ocorrido tenha a probabilidade de sucesso indicada com os dados fonecidos.
Esse experimento fornece indícios de que houveram um numero significativo de casos falso positivos na Microrregião de Itabira, devido sua baixa letalidade e um alto indice de casos confirmados comparado com sua região.


Obs: Análise feita com os dados de infecção da população disponiveis no dia 25/06/2020.
