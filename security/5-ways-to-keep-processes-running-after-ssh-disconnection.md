Title: 5 Ways to Keep Processes Running After SSH Disconnection
Date: 2016-10-02 21:49:38
Category: security
Tags: disown, nohup, screen, setsid, ssh, tmux
Slug:5-ways-to-keep-processes-running-after-ssh-disconnection
Authors:sedlav
Summary: When we log out of the session or the session times out after being idle for quite some time, the SIGHUP signal is send to the pseudo-terminal and 

> 
When we log out of the session or the session times out after being idle for quite some time, the SIGHUP signal is send to the pseudo-terminal and all the jobs that have been run on that terminal, even the jobs that have their parent jobs being initiated on the pseudo-terminal are also sent the SIGHUP signal and are forced to terminate.
Only the jobs that have been configured to ignore this signal are the ones that survive the session termination.

[Link](http://www.tecmint.com/keep-remote-ssh-sessions-running-after-disconnection/)
