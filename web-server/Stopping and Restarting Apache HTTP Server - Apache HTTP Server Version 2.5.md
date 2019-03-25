---
title: Stopping and Restarting Apache HTTP Server - Apache HTTP Server Version 2.5
date: 2019-03-25 13:17:22
categories: [web server]
tags: [apache, httpd]
authors: sedlav
---
        
In order to stop or restart the Apache HTTP Server, you must send a signal to the running httpd processes. There are two ways to send the signals. First, you can use the unix kill command to directly send signals to the processes. You will notice many httpd executables running on your system, but you should not send signals to any of them except the parent, whose pid is in the PidFile. That is to say you shouldn't ever need to send signals to any process except the parent. There are four signals that you can send the parent: TERM, USR1, HUP, and WINCH, which will be described in a moment.

[Link](https://httpd.apache.org/docs/trunk/stopping.html)
