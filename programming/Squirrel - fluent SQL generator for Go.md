---
Title: "Squirrel - fluent SQL generator for Go"
Date: 2018-01-29 11:25:19
Categories: [programming]
Tags: [go, squirrel]
Authors: sedlav
---

Squirrel is not an ORM. Squirrel helps you build SQL queries from composable parts:

```go
import sq "github.com/Masterminds/squirrel"

users := sq.Select("*").From("users").Join("emails USING (email_id)")

active := users.Where(sq.Eq{"deleted_at": nil})

sql, args, err := active.ToSql()

sql == "SELECT * FROM users JOIN emails USING (email_id) WHERE deleted_at IS NULL"
```

[Link](https://github.com/Masterminds/squirrel)
