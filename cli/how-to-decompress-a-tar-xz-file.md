---
Title: "How to decompress a tar.xz file?"
Date: 2016-08-30 02:26:33
Categories: [cli]
Tags: [tar]
Slug: how-to-decompress-a-tar-xz-file
Authors: sedlav
---

You must use the tar tool with J option

```
$ tar xJvf php-7.0.10.tar.xz</code></pre>
```

Where:

x = extract
f = file
v = verbose
J = Filter the archive through xz
