---
Title: How to watch for specific pattern in a log file.
Date: 2017-03-01 12:08:52
Categories: [cli]
tags: [tail, grep]
Authors: sedlav
---

You must combine tail and grep in this way:

```
# tail -f log_file | grep pattern
```

For example looks for a specific IP in Apache log.

```
# tail -f /var/log/httpd/access_log | grep IP-address
```
