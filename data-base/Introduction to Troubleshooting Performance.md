---
Title: "Introduction to Troubleshooting Performance/Slow queries"
Date: 2016-11-16 17:18:00
Categories: [data base]
tags: [percona, mysql, mariadb]
Authors: sedlav
---

Sveta Smirnova provides a guide for Troubleshooting Performance/Slow queries. Here are some of the questions answered by Sveta Smirnova:

* I’ve heard that is a bad idea to use select *, what do you recommend?
* If there is a compound index like index1(emp_id,date), will the following query be able to use index? “select * from table1 where emp_id = 10”
* Finally, only certain composite indexes were suitable, the column order in the complex index mattered a lot. Why couldn’t the optimizer merge the four individual single column indexes, and why did the order of the columns in the composite index matter?

[Link](https://www.percona.com/blog/2016/05/20/introduction-troubleshooting-performance-troubleshooting-slow-queries-webinar-q/)
