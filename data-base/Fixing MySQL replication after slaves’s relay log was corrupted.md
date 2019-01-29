---
Title: "Fixing MySQL replication after slaves’s relay log was corrupteds"
Date: 2019-01-29 18:06:04
Categories: [data base]
tags: [mysql, mariadb, percona]
Authors: sedlav
---

MySQL replication on slave (version 5.1.61) has stopped. Slave_IO_Running was marked as Yes, but Slave_SQL_Running as No. Simple stop/start slave didn’t help so further problem analysis was needed.

[Link](https://www.redips.net/mysql/replication-slave-relay-log-corrupted/)
