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
Filter for the names Steven, Thomas, and Matthew
```
names_filtered <- names_normalized %>%
 filter(name==c("Steven", "Thomas", "Matthew")) %>%
 ```
#### 2.dplyr Join Two table together:
inner_join:
<br>Use the suffix argument to replace .x and .y suffixes
```
parts %>% 
	inner_join(part_categories, by = c("part_cat_id" = "id"), suffix = c("_part", "_category"))
```
Joining three tables
```
sets %>%
	inner_join(inventories, by = "set_num") %>%
	inner_join(inventory_parts, by = c("id" = "inventory_id"))
```

Count the name_color column and sort the results so the most prominent colors appear first.
```
count(name_color, sort=TRUE)
```

left_join

Combine the star_destroyer and millennium_falcon tables with the suffixes _falcon and _star_destroyer.
 ```
millennium_falcon %>%
  left_join(star_destroyer, by = c("part_num", "color_id"), suffix = c("_falcon", "_star_destroyer"))
```  
right_join
```
parts %>%
	count(part_cat_id) %>%
	right_join(part_categories, by = c("part_cat_id" = "id")) %>%
	# Filter for NA
	filter(is.na(n))
```
replace_na
```
# Use replace_na to replace missing values in the n column
	replace_na(list(n = 0))
```
full_join

```
batman_parts %>%
  # Combine the star_wars_parts table 
  full_join(star_wars_parts, by = c("part_num", "color_id"), suffix = c("_batman", "_star_wars")) %>%
  # Replace NAs with 0s in the n_batman and n_star_wars columns 
  replace_na(list(n_batman = 0, n_star_wars = 0))
```
semi_join
```
# Filter the batwing set for parts that are also in the batmobile set
batwing %>%
  semi_join(batmobile, by = c("part_num"))
```
anti_join
```
# Filter the batwing set for parts that aren't in the batmobile set
batwing %>%
  anti_join(batmobile, by = c("part_num"))
``` 

References:

Join two tbls together
<br>https://dplyr.tidyverse.org/reference/join.html

Join two tables
<br>https://stat545.com/join-cheatsheet.html#the-data
