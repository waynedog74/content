---
Title: "Using Unbound for recursive DNS lookup"
Date: 2017-03-12 11:24:22
Categories: [network]
tags: [unbound, dns]
Authors: sedlav
---

Some organizations decide to use its internal authoritative DNS servers as recursive DNS because of easiness and reverse lookup of internal RFC 1918 networks works out of the box. That should be avoided for (at least) two reasons:

* Cache poisoning can cause security nightmares
* Authoritative answers are never cached and can cause a high load on the DNS servers.

[Link](https://blog.delouw.ch/2017/03/09/using-unbound-for-recursive-dns-loopup/)
