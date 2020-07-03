---
title: "Paired samples t-test"
output: 
  html_document:
    keep_md: yes
---

The code below simulates the running speed of someone before and after drinking x ammount of coffee.


```r
names <- c()
for(i in 1:10){
  name <- paste('participant', i)
  names[i] <- name
}
before_coffee = seq(from = 5, to = 50, by = 5) + rnorm(n = 10, mean = 1, sd = 2)
coffee_sim <- data.frame( "Participants" = c(names),
                          "before_coffee" = before_coffee,
                          "after_coffee" = before_coffee + rnorm(n = 10, mean = 20, sd = 1)
)
```

Imagine you are a researcher and you want to measured the speed 
of a pearson running before and after a cup of coffee. Here's your data set. Take a look at it
compare the differences in both within subject (row to row), 
and within conditions (column to column):


```r
coffee_sim
```

```
##      Participants before_coffee after_coffee
## 1   participant 1       7.15019     28.49564
## 2   participant 2      12.61597     32.20233
## 3   participant 3      16.38833     38.07997
## 4   participant 4      22.92365     42.56995
## 5   participant 5      26.76184     48.96162
## 6   participant 6      27.62871     48.06843
## 7   participant 7      37.74125     58.60364
## 8   participant 8      42.20998     62.18529
## 9   participant 9      44.44015     64.52535
## 10 participant 10      50.75972     71.03978
```
2) Calculate the descriptive statistics that we learned in our previous exercises


```r
mean(coffee_sim$before_coffee)
```

```
## [1] 28.86198
```

```r
mean(coffee_sim$after_coffee)
```

```
## [1] 49.4732
```

```r
sd(coffee_sim$before_coffee)
```

```
## [1] 14.57289
```

```r
sd(coffee_sim$after_coffee)
```

```
## [1] 14.35535
```
3) Using only the descriptive statistics from question 2, 
#do you think that there will be a significance difference
#in speed before and after people take coffe? Justify your answer.


4) Calculate the difference in scores between conditions:


```r
dif <- mean(coffee_sim$before_coffee - coffee_sim$after_coffee)
```

#5) Calculate the standard error of the mean of the differences


```r
se_mean <- sd(coffee_sim$before_coffee - coffee_sim$after_coffee)/sqrt(length(coffee_sim$before_coffee))
```

#6) Now divide the difference you found between samples with the S.E.


```r
dif/se_mean
```

```
## [1] -73.41113
```

#7) Now compute a paired samples t-test using r's native function. Compare the t-statistic with the result from question 6

```r
t.test(coffee_sim$after_coffee,
       coffee_sim$before_coffee,
       paired = TRUE)[["statistic"]][["t"]]
```

```
## [1] 73.41113
```
