---
Title: "The Impact of Swapping on MySQL Performance"
Date: 2017-01-13 17:17:00
Categories: [data base]
Tags: [mysql, mariadb, percona]
Authors: sedlav
---

It’s common sense that when you’re running MySQL (or really any other DBMS) you don’t want to see any I/O in your swap space. Scaling the cache size (using innodb_buffer_pool_size in MySQL’s case) is standard practice to make sure there is enough free memory so swapping isn’t needed.

[Link](https://www.percona.com/blog/2017/01/13/impact-of-swapping-on-mysql-performance/)
