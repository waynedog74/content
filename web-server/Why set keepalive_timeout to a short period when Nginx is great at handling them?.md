---
Title: "Why set keepalive_timeout to a short period when Nginx is great at handling them?"
Date: 2017-12-05 11:49:57
Categories: [web server]
tags: [nginx, performance]
Authors: sedlav
---

Keep alive is a HTTP feature which allows user agents to keep the connection to your server open for a number of requests or until the specified time out is reached. This won’t actually change the performance of our nginx server very much as it handles idle
connections very well.

[Link](https://www.ruby-forum.com/topic/6878679)
