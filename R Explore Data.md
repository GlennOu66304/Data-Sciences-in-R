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

### In R markdwon , If you want to run R Code at command line as the with a R scipt, Like you do not want to see plot inlie, you could Click Seting section symbol (next to Knit),Then choose Chunk out put in console.you can see the location as image below:
![ ](https://github.com/GlennOu66304/Data-Sciences-in-R/blob/R-Learning/image/Allow%20R%20markdown%20content%20in%20console%20contetn.png)
### Comment: If you look for answers in Video Include:Youtube,Bilibili,Mooc Platform, You need to use 1080P Video quality to find answer part you are looking for.

Blogs:
1.ggplot2 tutorial by Ramon Saccilotto
<br>http://bbs.ceb-institute.org/wp-content/uploads/2011/09/handout_ggplot2.pdf
<br>2.Earning R by imitation
<br>https://rollingyours.wordpress.com/
<br>3.R Blogger
<br>https://www.r-bloggers.com/hadley-wickham-presents-dplyr-at-user-2014/
