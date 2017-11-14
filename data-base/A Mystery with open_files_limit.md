---
Title: "A Mystery with open_files_limit"
Date: 2017-11-09 11:08:44
Categories: [data base]
Tags: [mysql, mariadb, percona]
Authors: sedlav
---

Like many database management systems, MySQL uses logs to achieve data durability (when using the default InnoDB storage engine). This ensures that when a transaction is committed, data is not lost in the event of crash or power loss.

[Link](https://www.percona.com/blog/2017/10/12/open_files_limit-mystery/)
