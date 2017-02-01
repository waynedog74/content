---
Title: Linux commands to put files and directory permissions on LAMP stack
Date: 2016-09-14 18:11:59
Categories: [cli]
tags: [apache, chgrp, chown, find, nginx]
Slug: files-and-directory-permissions-for-lamp-stack
Authors: maikelgon
---

If you want to fix files permission on you LAMP stack you can execute following commands:

```
cd /var/www/mysite.com
chown -R apache *
chgrp -R apache *
# Set directories permission to owner=rwx, group=rx,other=rx
find /var/www/mysite.com/ -type d -exec chmod 755 {}
# Set file permission to owner=rw, group=r,other=r
find /var/www/mysite.com/ -type f -exec chmod 644 {}
# Full permissions for every body for cache dir
chmod -R 777 /var/www/mysite.com/tmp
```

Use the last sentence for cache or tmp directory that need all permissions enabled.

For NGINX server change the username apache for nginx.

Generally above operation should be done as root.
