---
Title: "Handling Composer \"lock file out of date\" Warning"
Date: 2017-01-29 14:40:52
Categories: [programming]
Tags: [php]
Authors: sedlav
---

Composer is dependency management for PHP, and it consists of two main files:

* composer.json where you specify your dependencies
* composer.lock where composer itself records exactly which precise version of every library and every dependency of every library it picked, so all installs will be identical

Crucially, the composer.lock also includes a hash of the current composer.json when it updates, so you can always tell if you've added a requirement to the composer.json file and forgotten to install it.

In that case, you'll see an error message like:

```
Warning: The lock file is not up to date with the latest changes in composer.json. You may be getting outdated dependencies. Run update to update them.
```

[Link](https://lornajane.net/posts/2016/handling-composer-lock-file-out-of-date-warning)
