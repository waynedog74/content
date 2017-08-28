---
Title: "Go database sql tutorial"
Date: 2017-08-28 12:13:34
Categories: [programming]
Tags: [go]
Authors: sedlav
---

## Revel: A high-productivity web framework for the Go language.

To access databases in Go, you use a sql.DB. You use this type to create statements and transactions, execute queries, and fetch results.

The first thing you should know is that a sql.DB isn’t a database connection. It also doesn’t map to any particular database software’s notion of a “database” or “schema.” It’s an abstraction of the interface and existence of a database, which might be as varied as a local file, accessed through a network connection, or in-memory and in-process.

[Link](http://go-database-sql.org/index.html)
