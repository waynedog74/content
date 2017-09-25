---
Title: "How to Change Runlevels (targets) in SystemD"
Date: 2017-09-24 23:10:00
Categories: [os]
Tags: [runlevels, systemd]
Authors: sedlav
---

In this article, we will explain how to change runlevels (targets) with systemd. Before we move any further, let’s briefly under the relationship between runlevels numbers and targets.

* Run level 0 is matched by poweroff.target (and runlevel0.target is a symbolic link to poweroff.target).
* Run level 1 is matched by rescue.target (and runlevel1.target is a symbolic link to rescue.target).
* Run level 3 is emulated by multi-user.target (and runlevel3.target is a symbolic link to multi-user.target).
* Run level 5 is emulated by graphical.target (and runlevel5.target is a symbolic link to graphical.target).
* Run level 6 is emulated by reboot.target (and runlevel6.target is a symbolic link to reboot.target).
* Emergency is matched by emergency.target.

[Link](https://www.tecmint.com/change-runlevels-targets-in-systemd/)
