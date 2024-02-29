---
title: "3uzd"
output: html_document
date: "2024-02-28"
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```

## 3 užduotis

3. Transformuokite duomenų failą donate.sas7bdat į tvarkingą duomenų failą, tam suskurkite
naują kintamąjį donate_rate.


```{r}
library(sas7bdat)
donate=read.sas7bdat("C:/Users/emile/Downloads/donate.sas7bdat")
library(tidyr)
donate%>%
pivot_longer(c(Qtr1, Qtr2, Qtr3, Qtr4), names_to = "Qtr", values_to = "donate_rate")

