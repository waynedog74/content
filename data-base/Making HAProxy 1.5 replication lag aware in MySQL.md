---
Title: "Making HAProxy 1.5 replication lag aware in MySQL"
Date: 2016-11-11 15:47:00
Categories: [data base]
Tags: [mysql, mariadb, percona]
Authors: sedlav
---

> HAProxy is frequently used as a software load balancer in the MySQL world. Peter Boros, in a past post, explained how to set it up with Percona XtraDB Cluster (PXC) so that it only sends queries to available nodes. The same approach can be used in a regular master-slaves setup to spread the read load across multiple slaves. However with MySQL replication, another factor comes into play: replication lag.

[Link](http://www.percona.com/blog/2014/12/18/making-haproxy-1-5-replication-lag-aware-in-mysql/)
