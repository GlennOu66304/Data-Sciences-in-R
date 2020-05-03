# R Explore Data.
## Histgram
Quick plot
<br>https://ggplot2.tidyverse.org/reference/qplot.html
```
setwd('/Users/zhanghuiqiao/Downloads')
pf <- read.csv('pseudo_facebook.tsv', sep = '\t')
names(pf)
install.packages('ggplot2')
library(ggplot2)

names(pf)
qplot(x = dob_day, data = pf)

```
ggplot
```
ggplot(aes(x = friend_count), data = pf) +
  geom_histogram() +
  scale_x_continuous(limits = c(0, 1000))
```

Run this code in R scrpt, The plot will be played in plot section, Run this code in R Markdown, The plot will be played in the R Markdown file inside.
