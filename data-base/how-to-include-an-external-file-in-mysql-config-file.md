---
Title: "How to include an external file in MySQL config file?"
Date: 2016-09-09 17:59:41
Categories: [data base]
Tags: [MariaDB, MySQL]
Slug: how-to-include-an-external-file-in-mysql-config-file
Authors: sedlav
---

You must use one of the following directives:

**!include** to include specific file

**!includedir** to include a whole directory.

Edit /etc/mysql/my.cnf

```mysql
# Include options found in myownfile.cnf
!include /etc/mysql/myownfile.cnf
# Include all confif found on myown.d dir
!includedir /etc/mysql/myown.d
```
