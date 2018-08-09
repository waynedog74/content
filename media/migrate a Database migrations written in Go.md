---
Title: "migrate, Database migrations written in Go."
Date: 2018-08-09 11:28:08
Categories: [media]
Tags: [go]
Authors: sedlav
---

Database migrations written in Go. Use as CLI or import as library.

- Migrate reads migrations from sources and applies them in correct order to a database.
- Drivers are "dumb", migrate glues everything together and makes sure the logic is bulletproof. (Keeps the drivers lightweight, too.)
- Database drivers don't assume things or try to correct user input. When in doubt, fail.

[Link](https://github.com/golang-migrate/migrate)
