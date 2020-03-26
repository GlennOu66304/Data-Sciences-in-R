### R_basic
#### 1.dplyr
Select the columns state, county, population, men, and women
```
counties_selected <- counties %>%
  select(state, county, population, men, women)
 ```
Use count to find the number of counties in each region
```
counties_selected %>%
  count(region, sort = TRUE)
  ```
