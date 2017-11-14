---
Title: "Avoid Shared Locks from Subqueries When Possible"
Date: 2017-11-14 15:48:03
Categories: [data base]
tags: [mysql, mariadb, percona]
Authors: sedlav
---

In this blog post, we’ll look at how to avoid shared locks from subqueries.

I’m pretty sure most of you have seen an UPDATE statement matching rows returned from a SELECT query:

```sql
update ibreg set k=1 where id in (select id from ibcmp where id > 90000);
```

This query, when executed with

```sql
autocommit=1
```

[Link](https://www.percona.com/blog/2017/09/25/avoid-shared-locks-from-subqueries-when-possible/)
