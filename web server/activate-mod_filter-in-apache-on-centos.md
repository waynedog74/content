Title: Activate mod_filter in Apache on CentOS
Date: 2016-08-19 15:08:43
Category: web server
Tags: Apache, httpd
Slug:activate-mod_filter-in-apache-on-centos
Authors:sedlav
Summary: When you install Apache HTTP on CentOS, mod_filter is not enabled by default then if you try to use some of its directives an error like this is rai

When you install Apache HTTP on CentOS, mod_filter is not enabled by default then if you try to use some of its directives an error like this is raised:

 "Invalid command 'FilterDeclare', perhaps misspelled or defined by a module not included in the server configuration",

so to resolve the above error is enough to add the following line to the httpd.conf:

The Apache HTTP Server Project is an effort to develop and maintain an open-source HTTP server for modern operating systems including UNIX and Windows. The goal of this project is to provide a secure, efficient and extensible server that provides HTTP services in sync with the current HTTP standards.

[Link](http://www.librebyte.net/en/apache/activate-mod_filter-in-apache-on-centos/)
