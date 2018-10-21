---
Title: "MySQL Skip Duplicate Replication Errorsr"
Date: 2018-10-21 17:13:15
Categories: [data base]
tags: [mysql, mariadb, percona, backup]
Authors: sedlav
---

Normally MySQL replication will stop whenever there is an error running a query on the slave. This happens in order for us to be able to identify the problem and fix it, and keep the data consistent with the mater that has sent the query. You can skip such errors, even if this is not recommended, as long as you know really well what are those queries and why they are failing, etc.

[Link](http://www.ducea.com/2008/02/13/mysql-skip-duplicate-replication-errors/)
