---
title: pg_rman - manages backup and recovery of PostgreSQL.
date: 2021-08-04 13:27:01
categories: [data base]
tags: [postgresql]
authors: sedlav
---

**pg_rman** has the features below:

- Takes a backup of entire database including tablespaces with just one command.
- Can recovery from backup with just one command.
- Supports incremental backup and compression of backup files so that it takes less disk spaces.
- Manages backup versions and shows a catalog of the backups.
- Supports storage snapshot.
- DATE is the start time of the target backup in ISO-format (YYYY-MM-DD HH:MI:SS). Prefix match is used to compare DATE and backup files.

[Link](https://ossc-db.github.io/pg_rman/index.html)
