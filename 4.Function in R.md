Note the arguments to median()
```
args(median)
```
Rewrite this function call, following best practices
<br>The x argument should come first.
<br>You don't need to name x, but you should name na.rm.
```
median(gold_medals, na.rm = TRUE)
```

Note the arguments to rank()
```
args(rank)
```
Rewrite this function call, following best practices
<br>The x argument should come first, then na.last, then ties.method.
<br>You don't need to name x, but you should name na.last and ties.method
```
rank(-gold_medals, na.last = "keep", ties.method = "min")
```
