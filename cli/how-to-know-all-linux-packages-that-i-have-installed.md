---
Title: How to know all Linux packages that I have installed?
Date: 2016-08-22 14:55:18
Categories: [cli]
tags: [dpkg-query]
Slug: how-to-know-all-linux-packages-that-i-have-installed
Authors: sedlav
---

If you are using Debian base distro you can type:

```
$ sudo dpkg-query -l '*linux*'
...
ii  linux-image-4.4.0-34-generic           4.4.0-34.53~14.04.1
ii  linux-image-extra-4.4.0-34-generic     4.4.0-34.53~14.04.1
ii  linux-image-generic-lts-xenial         4.4.0.34.24
...
```
