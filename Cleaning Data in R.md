## Cleaning Data in R  

### 1. Introduction and exploring raw data

View the first 6 rows of data
```
head(weather)
```
View the first 15 rows
```
head(bmi, 15)
```
View the last 6 rows of data
```
tail(weather)
```
View the last 10 rows
```
tail(bmi, 10)
```

View a condensed summary of the data
```
str(weather)
```
Check the class of bmi
```
class(bmi)
```
Check the dimensions of bmi
```
dim(bmi)
```
View the column names of bmi
```
names(bmi)
```
Load dplyr
```
library(dplyr)
```
Check the structure of bmi, the dplyr way
```
glimpse(bmi)
```

View a summary of bmi
```
summary(bmi)
```
Print the full dataset to the console
```
print(bmi)
```
