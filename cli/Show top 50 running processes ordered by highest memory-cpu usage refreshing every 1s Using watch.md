---
title: Show top 50 running processes ordered by highest memory-cpu usage refreshing every 1s Using watch
date: 2019-12-04 13:51:00
categories: [cli]
tags: [ps, watch,head]
authors: sedlav
---

```
watch -n1 "ps aux --sort=-%mem,-%cpu | head -n 50
```

[Link](https://www.commandlinefu.com/commands/view/24824/show-top-50-running-processes-ordered-by-highest-memorycpu-usage-refreshing-every-1s)
