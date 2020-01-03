---
title: sql.js,  SQLite compiled to JavaScript through Emscripten
date: 2020-01-03 10:13:19
categories: [data base]
tags: [sqlite, sql.js]
authors: sedlav
---

sql.js is a port of SQLite to Webassembly, by compiling the SQLite C code with Emscripten. It uses a virtual database file stored in memory, and thus doesn't persist the changes made to the database. However, it allows you to import any existing sqlite file, and to export the created database as a JavaScript typed array.

[Link](https://github.com/kripken/sql.js/)
