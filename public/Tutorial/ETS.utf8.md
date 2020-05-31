---
title: "ETS_exercise"
author: "Thiyanga Talagala"
date: "31/05/2020"
output: pdf_document
---




```r
library(forecast)
```

```
## Registered S3 method overwritten by 'quantmod':
##   method            from
##   as.zoo.data.frame zoo
```

```r
library(fpp2)
```

```
## Loading required package: ggplot2
```

```
## Loading required package: fma
```

```
## Loading required package: expsmooth
```


```r
ausair.tr <- window(ausair, end=2011)
ausair.tr
```

```
Time Series:
Start = 1970 
End = 2011 
Frequency = 1 
 [1]  7.31870  7.32660  7.79560  9.38460 10.66470 11.05510 10.86430 11.30650
 [9] 12.12230 13.02250 13.64880 13.21950 13.18790 12.60150 13.23680 14.41210
[17] 15.49730 16.88020 18.81630 15.11430 17.55340 21.86010 23.88660 26.92930
[25] 26.88850 28.83140 30.07510 30.95350 30.18570 31.57970 32.57757 33.47740
[33] 39.02158 41.38643 41.59655 44.65732 46.95177 48.72884 51.48843 50.02697
[41] 60.64091 63.36031
```

```r
ausair.test <- window(ausair, start=2012)
ausair.test
```

```
Time Series:
Start = 2012 
End = 2016 
Frequency = 1 
[1] 66.35527 68.19795 68.12324 69.77935 72.59770
```


```r
autoplot(ausair.tr)
```

![](ETS_files/figure-latex/unnamed-chunk-3-1.pdf)<!-- --> 

```r
ets(ausair.tr)
```

```
## ETS(M,A,N) 
## 
## Call:
##  ets(y = ausair.tr) 
## 
##   Smoothing parameters:
##     alpha = 0.9999 
##     beta  = 0.024 
## 
##   Initial states:
##     l = 6.5399 
##     b = 0.7358 
## 
##   sigma:  0.08
## 
##      AIC     AICc      BIC 
## 206.1828 207.8495 214.8712
```
