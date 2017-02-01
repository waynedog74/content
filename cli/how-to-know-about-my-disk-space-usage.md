---
Title: How to know about my disk space usage?
Date: 2016-08-22 15:12:35
Categories: [cli]
tags: [df]
Slug: how-to-know-about-my-disk-space-usage
Authors: sedlav
---

Type the following command:

```
$ df -h
Filesystem                       Size  Used Avail Use% Mounted on
udev                             3,9G   12K  3,9G   1% /dev
tmpfs                            788M  2,2M  786M   1% /run
/dev/dm-2                         20G  9,8G  8,4G  54% /
none                             4,0K     0  4,0K   0% /sys/fs/cgroup
none                             5,0M     0  5,0M   0% /run/lock
none                             3,9G   35M  3,9G   1% /run/shm
none                             100M   84K  100M   1% /run/user
/dev/mapper/lcmobile_group-home  894G  828G   21G  98% /home
```
