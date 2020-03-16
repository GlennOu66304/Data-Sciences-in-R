## Importing data from databases 
### 1. Enviroment Build:
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
### 2. SQL Query in R

 Use dbGetQuery() to create a data frame, elisabeth, that selects the tweat_id column from the comments table where elisabeth is the commenter, her user_id is 1
 
 As usual, you first pass the connection object to it. The second argument is an SQL query in the form of a character string. 
 
```
elisabeth <-  dbGetQuery(con, "SELECT tweat_id FROM comments  WHERE user_id = 1")
```
Print elisabeth
```
elisabeth
```
Import post column of tweats where date is higher than '2015-09-21': latest
```
latest <- dbGetQuery(con, "SELECT post FROM tweats WHERE date > '2015-09-21'")
```
AND :Create an R data frame, specific, that selects the message column from the comments table where the tweat_id is 77 and the user_id is greater than 4.
```
specific <- dbGetQuery (con,"SELECT message FROM comments WHERE tweat_id = 77 AND user_id > 4")
```
CHAR_LENGTH():Create a data frame, short, that selects the id and name columns from the users table where the number of characters in the name is strictly less than 5.
```
short <- dbGetQuery(con, "SELECT id,name FROM users WHERE CHAR_LENGTH(name) < 5")
```
Send query to the database
```
res <- dbSendQuery(con, "SELECT * FROM comments WHERE user_id > 4")
```

Use dbFetch() twice
In the first call, import only two records of the query result by setting the n argument to 2
```
dbFetch(res, n=2)
```
n the second call, import all remaining queries (don't specify n). In both calls, simply print the resulting data frames.
```
dbFetch(res)
```
Clear res
```
dbClearResult(res)
```
Disconnect from the database
```
dbDisconnect(con)
```
