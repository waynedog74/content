---
Title: "Is MySQL’s innodb_file_per_table slowing you down?"
Date: 2017-01-26 08:44:58
Categories: [data base]
Tags: [percona, mysql, mariadb]
Authors: sedlav
---

> MySQL’s innodb_file_per_table is a wonderful thing – most of the time. Having every table use its own .ibd file allows you to easily reclaim space when dropping or truncating tables. But in some use cases, it may cause significant performance issues.

[Link](http://www.percona.com/blog/2015/02/24/mysqls-innodb_file_per_table-slowing/)
