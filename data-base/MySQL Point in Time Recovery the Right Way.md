---
Title: "MySQL Point in Time Recovery the Right Way"
Date: 2017-11-09 11:03:08
Categories: [data base]
tags: [mysql, mariadb, percona]
Authors: sedlav
---

Sometimes we need to restore from a backup, and then replay the transactions that happened after the backup was taken. This is a common procedure in most disaster recovery plans, when for example you accidentally drop a table/database or run an update/delete without the “where” clause and lose data.

[Link](https://www.percona.com/blog/2017/10/23/mysql-point-in-time-recovery-right-way/)
