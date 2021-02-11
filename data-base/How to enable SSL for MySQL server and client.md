---
title: How to enable SSL for MySQL server and client
date: 2021-02-11 00:40:21
categories: [data base]
tags: [mysql,ssl]
authors: sedlav
---

When users want to have a secure connection to their MySQL server, they often rely on VPN or SSH tunnels. Yet another option for securing MySQL connections is to enable SSL wrapper on an MySQL server. Each of these approaches has its own pros and cons. For example, in highly dynamic environments where a lot of short-lived MySQL connections occur, VPN or SSH tunnels may be a better choice than SSL as the latter involves expensive per-connection SSL handshake computation.

[Link](https://www.xmodulo.com/enable-ssl-mysql-server-client.html)
