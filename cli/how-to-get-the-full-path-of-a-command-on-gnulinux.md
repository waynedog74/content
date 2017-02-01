---
Title: How to get the full path of a command on GNU/Linux?
Date: 2016-09-01 03:30:26
Categories: [cli]
tags: [which]
Slug: how-to-get-the-full-path-of-a-command-on-gnulinux
Authors: sedlav
---

You must use the **which** command:
```
$ which ls
alias ls='ls --quoting-style=literal --color'
/usr/bin/ls
```
