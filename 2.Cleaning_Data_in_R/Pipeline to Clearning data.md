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
