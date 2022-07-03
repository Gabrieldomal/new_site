---
title: "Proporcionalmente, o Quadrilátero Ferrífero tem mais casos confirmados do que o resto de Minas Gerais?"
date: 2020-03-14T23:35:27-03:00
draft: false
---Hipótese:
A incidência do coronavírus no Quadrilátero Ferrífero segue mesma distribuição que as pessoas confirmadas em Minas Gerais.<br>
Teste:
É possível verificar se conseguimos descrever quantas pessoas estão sendo contaminadas no Quadrilátero, utilizando a taxa de contaminação de Minas Gerais sem o Quadrilátero.
A população do quadrilátero foi subtraída da população de Minas para não contaminar os dados, tornando-os enviesados.

X ~ Binomial(n,p)

X = 4255 -- número de confirmados de Corona vírus no quadrilátero
ferrífero.<br>
n = 1456854 -- número da população do quadrilátero ferrífero.<br>
p = 0.0016 --probabilidade de sucesso (taxa de contaminados pela população em MINAS GERAIS fora quadrilátero)<br><br>
X ~ Binomial(1456854, 0.0016)

mean = 2331
SD = 48.2

Grafico probabilidades de evento:
![normal](/grafico_site_quadri.jpg)

(Quantidade de contaminados dada a população X probabilidade do evento ocorrer.)

Casos confirmados registrados: 4255<br>

fdp - P(X=4255) = 5.36e-280<br>
fda - P(X <=4255) = 0.999<br><br>


Hipótese nula = a probabilidade de sucesso de 0.0016 descreve a distribuição do Quadrilátero Ferrífero.<br>
Hipótese alternativa = a probabilidade de sucesso verdadeira não é 0.0016<br><br>

p-valor = 2.2e-16<br>
p-valor < 0.05 (Hipotese nula negada)<br><br>


95% IC (0.002833694 - 0.003009645)

Probabilidade de sucesso estimada: 0.0029 (Taxa de contaminação no quadrilátero)

Conclusão:
É improvável que o evento ocorrido tenha a probabilidade de sucesso indicada, ou seja a taxa de contaminação em Minas Gerais não consegue descrever o que acontece no Quadrilátero Ferrífero.

Também é possível inferir que a taxa de confirmados no Quadrilátero é superior a taxa de contaminados do restante de Minas Gerais.
Obs: Análise feita com os dados disponíveis no dia 25/06/2020 pelo Ministério da Saúde de Minas Gerais.

Também podemos ver:

Confirmados no Quadrilátero Ferrrífero.

![normal](/grafico_quadrilatero.png)

Confirmados em Minas Gerais e em Minas Gerais sem o Quadrilátero.

![normal](/Comparacao.png)
