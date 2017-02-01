---
Title: "log.io - Real-time log monitoring in your browser"
Date: 2016-09-07 15:30:31
Categories: [data processing]
tags: [logio]
Slug: log-io-real-time-log-monitoring-in-your-browser
Authors: sedlav
---

**log.io **is a Real-time log monitoring tool built on shoulder of node.js + socket.io.

How does it work?

Harvesters watch log files for changes, send new log messages to the server via TCP, which broadcasts to web clients via socket.io.

Log streams are defined by mapping file paths to a stream name in harvester configuration.

Users browse streams and nodes in the web UI, and activate (stream, node) pairs to view and search log messages in screen widgets.

[Link](http://logio.org/)
