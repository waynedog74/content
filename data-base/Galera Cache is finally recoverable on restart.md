---
Title: "Galera Cache is finally recoverable on restart"
Date: 2016-12-01 08:28:00
Categories: [data base]
Tags: [mysql, mariadb, percona]
Authors: sedlav
---

> This post describes how to recover Galera Cache (or gcache) on restart.

> Recently Codership introduced (with Galera 3.19) a very important and long awaited feature. Now users can recover Galera cache on restart.

> If you gracefully shutdown cluster nodes one after another, with some lag time between nodes, then the last node to shutdown holds the latest data. Next time you restart the cluster, the last node shutdown will be the first one to boot. Any followup nodes that join the cluster after the first node will demand an SST.

[Link](https://www.percona.com/blog/2016/11/30/galera-cache-gcache-finally-recoverable-restart/)
