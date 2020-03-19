## Pipeline to Clearning data

### 1.Removing redundant info

nrow() and ncol() return the number of rows and columns in a data frame, respectively.
First 5 rows of my_df
```
my_df[1:5, ] 
```
Fourth column of my_df
```
my_df[, 4]   
```
Alternatively, you can remove rows and columns using **negative indices**. For example

<br>Omit first 5 rows of my_df
```
my_df[-(1:5), ] 
```
Omit fourth column of my_df
```
my_df[, -4]   
```
Remove the first column of sales: sales2
```
sales2 <- sales[, 2:ncol(sales)]
```
Remove rows 1, 7, and 11 of mbta: mbta2
```
mbta2 <- mbta[-c(1, 7, 11), ]
```
Remove the first column of mbta2: mbta3
```
mbta3 <- mbta2[, -1]
```
Define vector of duplicate cols (don't change)
```
duplicates <- c(4, 6, 11, 13, 15, 17, 18, 20, 22, 
                24, 25, 28, 32, 34, 36, 38, 40, 
                44, 46, 48, 51, 54, 65, 158)
```
Remove duplicates from food: food2
```
food2 <- food[, -duplicates]
```
