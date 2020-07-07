---
title: "A letalidade do Vírus em Itabira é a mesma que no resto do Quadrilátero Ferrífero? Isso pode ser um indício de casos Falso-Positivos?"
date: 2020-06-14T23:35:27-03:00
draft: false
---Hipótese:
A letalidade do coronavírus em Itabira segue mesma distribuição que a letalidade no Quadrilátero Ferrífero.

Teste:
A letalidade no Quadrilátero Ferrífero será a proporção de óbitos por contaminados, retirando os casos ocorridos na Microrregião de Itabira. Deve-se retirar a região analisada para não tornar os dados enviesados. 
Com isso podemos verificar se é possível descrever o que ocorre na Microrregião de Itabira observando apenas o que ocorre no resto do Quadrilátero Ferrífero.

X ~ Binomial(n,p)

X = 2 -- Número de óbitos de Corona vírus na Microrregião de Itabira.

n = 1095 -- Número da população que testou positivo para coronavírus na Microrregião de Itabira

p = 0.021 -- probabilidade de sucesso (letalidade no Quadrilátero sem a microrregião de Itabira)

X ~ Binomial(1095, 0.021)

mean = 23

SD = 4.74

Gráfico probabilidades de evento:
![normal](/grafico_site_itabira.jpg)

(Quantidade de óbitos dada a população X probabilidade do evento ocorrer.)

Óbitos registrados: 2
z = -4.42

fdp - P(X=2) = 2.22e-08
fda - P(X >=2) = 0.999

Hipótese nula = a probabilidade de sucesso de 0.021 descreve a distribuição do Quadrilátero Ferrífero.
Hipótese alternativa = a probabilidade de sucesso verdadeira não é 0.021

p-valor = 4.06e-08
p-valor < 0.05 (Hipótese nula negada)

Conclusão:
É improvável que o evento ocorrido tenha a probabilidade de sucesso indicada com os dados fornecidos.
Esse experimento fornece indícios de que houveram um numero significativo de casos falso positivos na Microrregião de Itabira, dada sua baixa letalidade e alto número de casos confirmados em sua região.

Obs: Análise feita com os dados disponíveis no dia 25/06/2020 pelo Ministério da Saúde de Minas Gerais.
