---
Title: "How Life360 Used ProxySQL to Lower Its Database Load"
Date: 2017-11-16 12:25:17
Categories: [data base]
tags: [mysql, mariadb, percona]
Authors: sedlav
---

> I’ve blogged before about one of our regular clients, Life360. One of the issues they recently had was the PING command taking about 30%-40% of total queries per second across their database infrastructure. This is a non-trivial amount and was easily tens of thousands of pings per second. This added a significant amount of latency to real queries.

[Link](https://www.percona.com/blog/2017/09/01/life360-used-proxysql-lower-database-load/)
