### 1. Importing data from databases 
Load the DBI package
```
library(DBI)
```
The dbConnect() call to connect to the MySQL database. Change the port argument (3306) and user argument ("student").
```
con <- dbConnect(RMySQL::MySQL(), 
                 dbname = "tweater", 
                 host = "courses.csrrinzqubik.us-east-1.rds.amazonaws.com", 
                 port = 3306,
                 user = "student",
                 password = "datacamp")
```
Build a vector of table names: tables
```
tables <- dbListTables(con)
```

Display structure of tables
```
str(tables)
```
Import the users table from tweater: users
```
users <- dbReadTable(con,"users")
```

Print users
```
users
```
Get table names
```
table_names <- dbListTables(con)
```
Import all tables,The first argument in lapply() should be the table names. The second argument is the function you want to execute for each of these table names, so dbReadTable.
```
tables <- lapply(table_names, dbReadTable, conn = con)
```
Print out tables
```
str(tables)
```
