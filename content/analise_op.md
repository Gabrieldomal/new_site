---
title: "O Quadrilátero Ferrífero tem mais casos confirmados, proporcionalmente, do que o resto de Minas Gerais?"
date: 2020-06-14T23:35:27-03:00
draft: false
images:
  - https://picsum.photos/1024/768/?random
---Hipotese:
A quantidade de obitos confirmados por coronavírus em itabira seguem mesma distribuição que a letalidade no Quadrilátero Ferrífero.

Teste:
É possivel verificar se conseguimos descrever quantos casos evoluiram para óbito, utilizando a letalidade do Quadrilátero Ferrífero sem a microrregião de Ouro Preto.
A população da Microrregião foi subtraida da população do Quadrilátero para não contaminar os dados, tornando-os enviesados.

X ~ Binomial(n,p)
z
X = 12 -- número de obitos de Corona vírus na Microrregião de Ouro Preto.

n = 1095 -- número da população da Microrregião de Ouro Preto.

p = 0.017 -- probabilidade de sucesso (letalidade no Quadrilátero sem a microrregião de Ouro Preto)

X ~ Binomial(1095, 0.017)

mean = 17

SD = 4.13

Grafico probabilidades de evento:
![normal](/grafico_site_op.jpg)

(Quantidade de óbitos dada a população de contaminados X probabilidade do evento ocorrer.)

Casos de óbito registrados: 12
fdp - P(X=12) = 0.04
fdp - P(X >=12) = 0.88

Hipótese nula = a probabilidade de sucesso de 0.017 descreve a distribuição do Quadrilátero Ferrífero.
Hipótese alternativa = a probabilidade de sucesso verdadeira não é 0.0017

p-valor = 0.2258
p-valor > 0.05 (Hipotese nula comprovada)

Conclusão:
É provavel que o evento ocorrido tenha a probabilidade de sucesso indicada com os dados fonecidos.
Esse experimento fornece indícios de que a distribuição da letalidade de coronavirus na microrregião de Ouro preto é representativa da amostra de letalidade da região do Quadrilátero Ferrífero.


Obs: Análise feita com os dados de infecção da população disponiveis no dia 25/06/2020.