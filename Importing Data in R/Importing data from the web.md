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
