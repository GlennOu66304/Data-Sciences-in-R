### Pipeline to import data case
Load readxl
```
library(readxl)
```

Import mbta.xlsx and skip first row: mbta
```
mbta <- read_excel("mbta.xlsx", skip = 1)
```
