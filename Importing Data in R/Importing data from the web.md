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
