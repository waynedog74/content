---
Title: "OpenSSH Multiplexer To Speed Up OpenSSH Connections"
Date: 2017-01-12 13:31:00
Categories: [security]
Tags: [OpenSSH]
Authors: sedlav
---

Multiplexing is nothing but send more than one ssh connection over a single connection. OpenSSH can reuse an existing TCP connection for multiple concurrent SSH sessions. This results into reduction of the overhead of creating new TCP connections.

[Link](https://www.cyberciti.biz/faq/linux-unix-osx-bsd-ssh-multiplexing-to-speed-up-ssh-connections/)
