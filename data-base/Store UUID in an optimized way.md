---
Title: "Store UUID in an optimized way"
Date: 2016-11-11 15:47:00
Categories: [data base]
tags: [mysql, mariadb, percona]
Authors: sedlav
---

> Many people store UUID as char (36) and use as row identity value (PRIMARY KEY) because it is unique across every table, every database and every server and allow easy merging of records from different databases. But here comes the problem, using it as PRIMARY KEY causes the problems described below.

[Link](http://www.percona.com/blog/2014/12/19/store-uuid-optimized-way/)
