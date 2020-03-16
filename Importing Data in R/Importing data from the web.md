## Importing data from the web

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
