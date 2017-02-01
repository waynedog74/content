---
Title: "Load balancing with ProxySQL"
Date: 2016-11-22 18:50:00
Categories: [data base]
tags: [mysql, mariadb, percona, proxysql]
Authors: sedlav
---

> ProxySQL is a high-performance SQL proxy. ProxySQL runs as a daemon watched by a monitoring process. The process monitors the daemon and restarts it in case of a crash to minimize downtime. The daemon accepts incoming traffic from MySQL clients and forwards it to backend MySQL servers. The proxy is designed to run continuously without needing to be restarted. Most configuration can be done at runtime using queries similar to SQL statements. These include runtime parameters, server grouping, and traffic-related settings.

[Link](https://www.percona.com/doc/percona-xtradb-cluster/LATEST/howtos/proxysql.html)
