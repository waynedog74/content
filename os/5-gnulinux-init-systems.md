Title: 5 GNU/Linux init systems
Date: 2016-08-11 14:41:49
Category: os
Tags: init
Slug:5-gnulinux-init-systems
Authors:sedlav
Summary: In Linux and other Unix-like operating systems, the init (initialization) process is the first process executed by the kernel at boot time. It has a

> In Linux and other Unix-like operating systems, the init (initialization) process is the first process executed by the kernel at boot time. It has a process ID (PID) of 1, it is executed in the background until the system is shut down.
The init process starts all other processes, that is daemons, services and other background processes, therefore, it is the mother of all other processes on the system. A process can start many other child processes on the system, but in the event that a parent process dies, init becomes the parent of the orphan process.

[Link](http://www.tecmint.com/best-linux-init-systems)
