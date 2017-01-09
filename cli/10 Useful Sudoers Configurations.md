---
Title: 10 Useful Sudoers Configurations
Date: 2017-01-09 17:16
Category: cli
Tags: sudo, sudoers
Authors: sedlav
---

> sudo allows a permitted user to execute a command as root (or another user), as specified by the security policy:

* It reads and parses /etc/sudoers, looks up the invoking user and its permissions,
* then prompts the invoking user for a password (normally the user’s password, but it can as well be the target user’s password. Or it can be skipped with NOPASSWD tag),
* after that, sudo creates a child process in which it calls setuid() to switch to the target user
* next, it executes a shell or the command given as arguments in the child process above.

[Link](http://www.tecmint.com/sudoers-configurations-for-setting-sudo-in-linux/)
