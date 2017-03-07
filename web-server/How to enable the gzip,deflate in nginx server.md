---
Title: "How to enable the gzip,deflate in nginx server"
Date: 2017-03-06 20:39:56
Categories: [web server]
tags: [nginx, gzip, deflate]
Authors: sedlav
---

You need to use the ngx_http_gzip_module module. It compresses all valid HTTP responses (files) using the “gzip” method. This is useful to reduce data transfer size and speed up web pages for static assets such as JavaScript, CSS files and more.

[Link](https://www.cyberciti.biz/faq/how-to-enable-the-gzipdeflate-in-nginx-server-on-linux-or-unix-system/)
