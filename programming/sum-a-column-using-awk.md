---
Title: "How to Sum a column using awk"
Date: 2016-08-09 20:30:44
Categories: [programming]
tags: [awk]
Slug: sum-a-column-using-awk
Authors: sedlav
---

If you want to get the total for a numeric column you can use awk, for example if we have the following file

```
$ cat stat.txt
Jan  124
Feb  929
Mar  708
Apr  947
```

then you can use awk in this way

```$ awk '{ SUM += $2} END { print SUM }' stat.txt```

Result = 2708
