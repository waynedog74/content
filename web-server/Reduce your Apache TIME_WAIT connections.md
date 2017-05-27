---
Title: "Reduce your Apache TIME_WAIT connections"
Date: 2017-05-26 21:19:19
Categories: [web server]
tags: [apache, httpd]
Authors: sedlav
---

> If you manage an Apache server, you may be noticing a large amount of TIME_WAIT connections all of the time. Don't get me wrong, TIME_WAIT is a good thing.. it basically means that your server has closed the connection, but it's being kept around so any delayed packets matched to the connection can be handled properly. We can reduce them, however.

[Link](https://www.linux.org/threads/reduce-your-apache-time_wait-connections.4505/)
