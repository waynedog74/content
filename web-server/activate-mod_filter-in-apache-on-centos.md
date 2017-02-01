---
Title: "Activate mod_filter in Apache on CentOS"
Date: 2016-08-19 15:08:43
Categories: [web server]
tags: [apache, httpd]
Slug: activate-mod_filter-in-apache-on-centos
Authors: sedlav
---

When you install Apache HTTP on CentOS, mod_filter is not enabled by default then if you try to use some of its directives an error like this is raised:

```
Invalid command 'FilterDeclare', perhaps misspelled or defined by a module not included in the server configuration
```

so to resolve the above error is enough to add the following line to the httpd.conf:

[Link](http://www.librebyte.net/en/apache/activate-mod_filter-in-apache-on-centos/)
