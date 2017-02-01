---
Title: "How to create a  file on the fly on GNU/Linux?"
Date: 2016-08-28 00:01:01
Categories: [cli]
tags: [touch]
Slug: how-to-create-file-on-the-fly-on-gnulinux
Authors: sedlav
---

You must use the **touch** command or **>** operator, the touch command will create an empty file while **>** also can put content on the file

###  Using touch command:

```
$ touch emptyfile.txt
```

### Using output redirector operator

```
$ echo -e "This an empty file\nwith a new line" > emptyfile.txt
```
