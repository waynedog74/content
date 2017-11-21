---
Title: "How to use special permissions: the setuid, setgid and sticky bits"
Date: 2017-11-21 09:36:07
Categories: [os]
Tags: [setuid, setgid, sticky bits]
Authors: sedlav
---

Normally, on a unix-like operating system, the ownership of files and directories is based on the default uid (user-id) and gid (group-id) of the user who created them. The same thing happens when a process is launched: it runs with the effective user-id and group-id of the user who started it, and with the corresponding privileges. This behavior can be modified by using special permissions.

[Link](https://linuxconfig.org/how-to-use-special-permissions-the-setuid-setgid-and-sticky-bits)
