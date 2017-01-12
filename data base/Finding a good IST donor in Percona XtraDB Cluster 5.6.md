---
Title: Finding a good IST donor in Percona XtraDB Cluster 5.6
Date: 12-01-2016 08:46
Category: data base
Tags: mysql, mariadb, percona
Authors: sedlav
---

> The Gcache is a memory-based cache of recent Galera transactions that is local to each node in a cluster.  If a node leaves and rejoins the cluster, it can use the gcache from another node that stayed in the cluster (i.e., its donor node) to fetch the transactions it missed (IST) as opposed to doing a full state snapshot transfer (SST).  However, there are a few nuances that are not obvious to the beginner:

[Link](https://www.percona.com/blog/2016/11/16/all-you-need-to-know-about-gcache-galera-cache/)
