---
Title: "ProxySQL Improves MySQL SSL Connections"
Date: 2017-11-16 12:16:16
Categories: [data base]
tags: [mysql, mariadb, percona, proxysql]
Authors: sedlav
---

When deploying MySQL with SSL, the main concern is that the initial handshake causes significant overhead if you are not using connection pools (i.e., mysqlnd-mux with PHP, mysql.connector.pooling in Python, etc.). Closing and making new connections over and over can greatly impact on your total query response time.

[Link](https://www.percona.com/blog/2017/09/19/proxysql-improves-mysql-ssl-connections/)
