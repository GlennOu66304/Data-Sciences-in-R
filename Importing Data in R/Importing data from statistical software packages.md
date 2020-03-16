## Importing data from statistical software packages
### 1.Import STATA data with haven
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
Import person.sav: traits
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
Convert work$GENDER to a factor
```
work$GENDER <- as_factor(work$GENDER)
```
### 2.Import STATA data with foreign
Load the foreign package
```
library(foreign)
```

Import florida.dta and name the resulting data frame florida
```
florida <- read.dta("florida.dta")
```

Check tail() of florida:last 6 observations of florida with tail()
```
tail(florida)
```
Specify the file path using file.path(): path
<br> file.path() takes 2 arguments in this case: the first one is the folder, "worldbank", and the second one is the file, "edequality.dta"
```
path <- file.path("worldbank","edequality.dta")
```
Create and print structure of edu_equal_1
```
edu_equal_1 <- read.dta(path)
str(edu_equal_1)
```
 Create and print structure of edu_equal_2
 ```
edu_equal_2 <- read.dta(path, convert.factors = FALSE)
str(edu_equal_2)
```
 Create and print structure of edu_equal_3
 ```
edu_equal_3 <- read.dta(path, convert.underscore = TRUE)
str(edu_equal_3)
```
