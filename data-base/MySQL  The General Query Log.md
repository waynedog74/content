---
Title: "MySQL The General Query Log"
Date: 2017-09-12 12:24:25
Categories: [data base]
tags: [mysql, mariadb, percona]
Authors: sedlav
---

The general query log is a general record of what mysqld is doing. The server writes information to this log when clients connect or disconnect, and it logs each SQL statement received from clients. The general query log can be very useful when you suspect an error in a client and want to know exactly what the client sent to mysqld.

[Link](https://dev.mysql.com/doc/refman/5.7/en/query-log.html)
