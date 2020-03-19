### Pipeline to import data case
##### 1.readxl
Load readxl
```
library(readxl)
```
Import mbta.xlsx and skip first row: mbta
```
mbta <- read_excel("mbta.xlsx", skip = 1)
```
##### 1.data.table
Load data.table
```
library(data.table)
```
Import food.csv as a data frame: food
```
food <- fread("food.csv",data.table=FALSE)
```
