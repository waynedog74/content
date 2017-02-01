---
Title: "Percona XtraDB Cluster 5.6: a tale of 2 GTIDs"
Date: 2017-01-26 08:39:23
Categories: [data base]
tags: [percona, mysql, mariadb]
Authors: sedlav
---

> Say you have a cluster with 3 nodes using Percona XtraDB Cluster (PXC) 5.6 and one asynchronous replica connected to node1. If asynchronous replication is using GTIDs, moving the replica so that it is connected to node2 is trivial, right? Actually replication can easily break for reasons that may not be obvious at first sight.

[Link](http://www.percona.com/blog/2015/02/13/percona-xtradb-cluster-5-6-a-tale-of-2-mysql-gtids/)
