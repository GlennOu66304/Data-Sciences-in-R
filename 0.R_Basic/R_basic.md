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
  Summarize to find minimum population, maximum unemployment, and average income
  ```
counties_selected %>%
 summarise(min_population=min(population),max_unemployment=max(unemployment),average_income=mean(income)) 
 ```
Group by region and find the greatest number of citizens who walk to work
```
counties_selected %>%
group_by(region) %>%
top_n(1,walk)
```
starts_with(). Another select helper is ends_with(), which finds the columns that end with a particular string.Select the state, county, population, and those ending with "work"
```
  select(state, county, population, ends_with("work")) %>% 
```
Rename the n column to num_counties
```
counties %>%
  count(state) %>%
  rename(num_counties = n)
  ```
Select state, county, and poverty as poverty_rate
```
counties %>%
   select(state, county, poverty_rate = poverty)
   ```
Keep the state, county, and populations columns, and add a density column
```
  transmute(state, county, population, density = population / land_area) %>%
```
