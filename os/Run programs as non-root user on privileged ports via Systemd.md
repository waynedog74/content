---
Title: "Run programs as non-root user on privileged ports via Systemd"
Date: 2018-01-12 10:40:03
Categories: [os]
tags: [init, systemd]
Authors: sedlav
---

Running programs as a non-root user is must in security sensitive environments. However, these programs sometimes need to publish their service on privileged ports like port 80 – which cannot be used by local users. Systemd offers a simple way to solve this problem.

[Link](https://liquidat.wordpress.com/2018/01/04/howto-run-programs-as-non-root-user-on-privileged-ports-via-systemd/)
