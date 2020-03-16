## Importing data from the web
### BASE:
Load the readr package
```
library(readr)
```

Import the csv file: pools
```
url_csv <- "http://s3.amazonaws.com/assets.datacamp.com/production/course_1478/datasets/swimming_pools.csv"
pools <- read_csv(url_csv)
```
Import the txt file: potatoes
```
url_delim <- "http://s3.amazonaws.com/assets.datacamp.com/production/course_1478/datasets/potatoes.txt"
potatoes <- read_tsv(url_delim)
```

Print pools and potatoes
```
pools
potatoes
```
Load the readxl and gdata package
```
library(readxl)
library(gdata)
```


Specification of url: url_xls
```
url_xls <- "http://s3.amazonaws.com/assets.datacamp.com/production/course_1478/datasets/latitude.xls"
```

Import the .xls file with gdata: excel_gdata
```
excel_gdata <- read.xls(url_xls)
```

 Download file behind URL, name it local_latitude.xls, download.file() requires two arguments: url, the URL you wish to download, and destfile, the destination file path. The latter is simply "local_latitude.xls".
 ```
local_latitude.xls <- download.file(url_xls,destfile="local_latitude.xls")
```

Import the local .xls file with readxl: excel_readxl
```
excel_readxl <- read_excel("local_latitude.xls")
```
Load the wine data into your workspace using load()
```
load("wine_local.RData")
```
Print out the summary of the wine data
```
summary(wine)
```
### HTTP? httr!
Load the httr package
```
library(httr)
```

Get the url, save response to resp
```
url <- "http://www.example.com/"
resp <- GET(url)
```
Print resp
```
resp
```

Get the raw content of resp: raw_content
```
raw_content <- content(resp,as="raw")
```

Print the head of raw_content
```
head(raw_content)
```
Print content of resp as text
```
content(resp,as="text")
```

Print content of resp
```
content(resp)
```
### API && JASON
Load the jsonlite package
```
library(jsonlite)
```

wine_json is a JSON
```
wine_json <- '{"name":"Chateau Migraine", "year":1997, "alcohol_pct":12.4, "color":"red", "awarded":false}'
```
Convert wine_json into a list: wine
```
wine <- fromJSON(wine_json)
```
Print structure of wine
 ```
str(wine)
```
Definition of quandl_url
```
quandl_url <- "https://www.quandl.com/api/v3/datasets/WIKI/FB/data.json?auth_token=i83asDsiWUUyfoypkgMz"
```
Import Quandl data: quandl_data
```
quandl_data <- fromJSON(quandl_url)
```
print structure of quandl_data
```
str(quandl_data)
```
Print out the Title element of both lists
```
sw4$Title
sw3$Title
```

Is the release year of sw4 later than sw3?
```
sw4$Year > sw3$Year 
```
