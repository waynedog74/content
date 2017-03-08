---
Title: How to execute specific command from the history.
Date: 2017-03-07 19:18:08
Categories: [cli]
tags: [bash, shell, history]
Authors: sedlav
---

Execute **history** command to see what command have you been executed.

```
$ history
...
 1996  linku2day
 1997  ls /var/log/httpd/access_log
 1998  sudo ls /var/log/httpd/access_log
 1999  linku2day
 2000  hugo server -t after-dark --buildDrafts
 2001  history
```

Now type:

```
$ !2000
```

To execute command number 2000 (hugo server -t after-dark --buildDrafts)


[Link](https://www.ossblog.org/5-highly-promising-terminal-emulators/)
