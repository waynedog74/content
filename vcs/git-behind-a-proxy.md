---
Title: Git behind a proxy
Date: 2016-08-11 15:01:54
Category: vcs
Tags: Git
Slug: git-behind-a-proxy
Authors: sedlav
Summary: If your sysadmin or SIP are blocking you (by using a proxy o firewall) still you can access remote Git repositories via http. You must add the followi
---

If your sysadmin or SIP are blocking you (by using a proxy o firewall) still you can access remote Git repositories via http. You must add the following lines to .git/config file.

```
[http]
proxy = http://user:pwd@proxy-url:proxy-port
# Useful if your proxy only allows known user agent
useragent = Mozilla/4.0
# Your repo Url
[remote "origin"]
url = https://github.com/company/project.git
fetch = +refs/heads/*:refs/remotes/htorigin/*
# This save your Github credential and avoid to type it over and over
[credential]
helper = store
```
