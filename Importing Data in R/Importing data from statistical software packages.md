### Importing data from statistical software packages
<br> SAS: read_sas()
<br> STATA: read_dta() (or read_stata(), which are identical)
<br> SPSS: read_sav() or read_por(), depending on the file type.
<br> Load the haven package

#### SAS
```
library(haven)
```
Import sales.sas7bdat: sales
```
sales <- read_sas("sales.sas7bdat")
```
Display the structure of sales
```
str(sales)
```
#### STATA
Import the data from the URL: sugar
```
sugar <- read_dta("http://assets.datacamp.com/production/course_1478/datasets/trade.dta")
```
Convert values in Date column to dates
```
sugar$Date <- as.Date(as_factor(sugar$Date))
```
Structure of sugar again
```
str(sugar)
```
#### SPSS
```
Import person.sav: traits
```
```
traits <- read_sav("person.sav") 
```

Summarize traits
```
summary(traits)
```

Print out a subset:
<br> subset of those individuals that scored high on Extroversion and on Agreeableness, i.e. scoring higher than 40 on each of these two categories
```
subset(traits, Extroversion > 40 & Agreeableness > 40)
```
