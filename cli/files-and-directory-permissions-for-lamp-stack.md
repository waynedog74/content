Title: Linux commands to put files and directory permissions on LAMP stack
Date: 2016-09-14 18:11:59
Category: cli
Tags: Apache, chgrp, chown, find, nginx
Slug:files-and-directory-permissions-for-lamp-stack
Authors:sedlav
Summary: <pre><code>cd /var/www/mysite.comchown -R apache *chgrp -R apache *find /var/www/mysite.com/ -type d -exec chmod 755 {} +find /var/www/mysite.com/

<pre><code>cd /var/www/mysite.com
chown -R apache *
chgrp -R apache *
find /var/www/mysite.com/ -type d -exec chmod 755 {} +
find /var/www/mysite.com/ -type f -exec chmod 644 {} +
chmod -R 777 /var/www/mysite.com/tmp
</code></pre>
Use the last sentence for cache or tmp directory that need all permissions enabled.
For NGINX server change the username apache for nginx.

