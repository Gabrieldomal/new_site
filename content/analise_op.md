---
title: "Proporcionalmente, a letalidade da Microrregião de Ouro Preto tem mais casos confirmados do que o resto do Quadrilátero Ferrífero?"
date: 2020-06-14T23:35:27-03:00
draft: false
---Hipótese:
A letalidade na Microrregião de Ouro Preto segue mesma distribuição que a letalidade no Quadrilátero Ferrífero.

Teste:
A letalidade no Quadrilátero Ferrífero será a proporção de óbitos por contaminados em Minas Gerais, retirando os casos ocorridos na Microrregião de Ouro Preto. Deve-se retirar a região analisada para não tornar os dados enviesados. 
Com isso podemos verificar se é possível descrever o que ocorre na na Microrregião de Ouro Preto observando apenas o que ocorre no resto do Quadrilátero Ferrífero.

X ~ Binomial(n,p)

X = 12 -- número de óbitos de Corona vírus na Microrregião de Ouro Preto.

n = 1025 -- número da população da Microrregião de Ouro Preto.

p = 0.017 -- probabilidade de sucesso (letalidade no Quadrilátero sem a microrregião de Ouro Preto)

X ~ Binomial(1025, 0.017)

mean = 17

SD = 4.13

Grafico probabilidades de evento:
![normal](/grafico_analise_op.png)

(Quantidade de óbitos dada a população de contaminados X probabilidade do evento ocorrer.)

Óbitos registrados: 12<br>
fdp - P(X=12) = 0.04<br>
fda - P(X >=12) = 0.88

Hipótese nula = a probabilidade de sucesso de 0.017 descreve a distribuição do Quadrilátero Ferrífero.<br>
Hipótese alternativa = a probabilidade de sucesso verdadeira não é 0.0017

p-valor = 0.2258<br>
p-valor > 0.05 (Hipótese nula comprovada)<br><br>

Conclusão:
É provavel que o evento ocorrido tenha a probabilidade de sucesso indicada com os dados fornecidos.
Esse experimento fornece indícios de que a distribuição da letalidade de coronavírus na microrregião de Ouro preto é representativa da amostra de letalidade da região do Quadrilátero Ferrífero.


Obs: Análise feita com os dados disponíveis no dia 25/06/2020 pelo Ministério da Saúde de Minas Gerais.