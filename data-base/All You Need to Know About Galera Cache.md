---
Title: "All You Need to Know About GCache (Galera-Cache)"
Date: 2016-12-01 08:31:00
Categories: [data base]
tags: [mysql, mariadb, percona]
Authors: sedlav
---

> This blog discusses some important aspects of GCache.

> Why do we need GCache?

> Percona XtraDB Cluster is a multi-master topology, where a transaction executed on one node is replicated on another node(s) of the cluster. This transaction is then copied over from the group channel to Galera-Cache followed by apply action.

> The cache can be discarded immediately once the transaction is applied, but retaining it can help promote a node as a DONOR node serving write-sets for a newly booted node.

> So in short, GCache acts as a temporary storage for replicated transactions.

[Link](https://www.percona.com/blog/2016/11/16/all-you-need-to-know-about-gcache-galera-cache/)
