---
Title: lf a terminal file manager
Date: 2017-01-17 09:16:16
Categories: [cli]
Tags: [lf, file manager]
Authors: sedlav
---

lf (as in "list files") is a terminal file manager written in Go. It is heavily inspired by ranger with some missing and extra features. Some of the missing features are deliberately omitted since it is better if they are handled by external tools.

Features:

* Cross-platform (Linux, OSX, BSDs, Windows (partial))
* Single binary without any runtime dependencies (except for terminfo database)
* Fast startup and low memory footprint (due to native code and static binaries)
* Server/client architecture to share file selection between multiple instances
* Custom commands as shell commands


[Link](https://github.com/gokcehan/lf)
