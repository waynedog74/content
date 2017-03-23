---
Title: How to print user, groups and ids for specifici user
Date: 2017-03-23 11:10:21
Categories: [cli]
tags: [id]
Authors: sedlav
---

Q. I want to know what is my user/groups id. What can I do?

A. Type id command

```
$ id username
```

You can omit the username for the current user

Example:

```
$ id
uid=1000(sedlav) gid=1000(sedlav) groups=1000(sedlav),10(wheel),48(apache),981(docker)
```

### Further reading:

* man id
