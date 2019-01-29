---
Title: "MySQL Server Error Codes and Messages"
Date: 2018-10-21 17:15:23
Categories: [data base]
tags: [mysql, mariadb, percona]
Authors: sedlav
---

**MySQL** programs have access to several types of error information when the server returns an error. For example, the mysql client program displays errors using the following format:

```mysql
shell> SELECT * FROM no_such_table;
ERROR 1146 (42S02): Table 'test.no_such_table' doesn't exist
The message displayed contains three types of information:
```

A numeric error code (1146). This number is MySQL-specific and is not portable to other database systems.

A five-character SQLSTATE value ('42S02'). The values are taken from ANSI SQL and ODBC and are more standardized. Not all MySQL error numbers have corresponding SQLSTATE values. In these cases, 'HY000' (general error) is used.

A message string that provides a textual description of the error.

[Link](https://dev.mysql.com/doc/refman/8.0/en/error-messages-server.html)
