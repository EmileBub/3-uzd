install.packages("tidyr")
install.packages("sas7bdat")
library(sas7bdat)
donate=read.sas7bdat("C:/Users/emile/Downloads/donate.sas7bdat")
library(tidyr)
donate%>%
pivot_longer(c(Qtr1, Qtr2, Qtr3, Qtr4), names_to = "Qtr", values_to = "donate_rate")
