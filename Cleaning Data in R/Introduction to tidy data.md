### 2.Introduction to tidy data

Apply gather() to bmi and save the result as bmi_long, This will create two new columns:
year, containing as values what are currently column headers.
bmi_val, the actual BMI values

```
bmi_long <- gather(bmi, year, bmi_val, -Country)
```
Use spread() to reverse the operation that you performed in the last exercise with gather(). In other words, 
make bmi_long wide again.
```
bmi_wide <- spread(bmi_long, year, bmi_val)
```
Apply the separate() function to bmi_cc
<br>Separate Country_ISO into two columns: Country and ISO
<br>Be sure to specify the correct separator with the sep argument
<br>Save the result to a new object called bmi_cc_clean
```
bmi_cc_clean <- separate(bmi_cc, col = "Country_ISO", into = c("Country", "ISO"), sep = "/")
```
View the first 20 rows of the result
```
head(bmi_long,20)
```
