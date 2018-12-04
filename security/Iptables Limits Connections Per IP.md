---
Title: "Iptables Limits Connections Per IP"
Date: 2018-12-04 09:51:07
Categories: [security]
tags: [iptables]
Authors: sedlav
---

Q. How do I restrict the number of connections used by a single IP address to my server for port 80 and 25 using iptables?

A. You need to use the connlimit modules which allows you to restrict the number of parallel TCP connections to a server per client IP address (or address block).

[Link](https://www.cyberciti.biz/faq/iptables-connection-limits-howto/)
