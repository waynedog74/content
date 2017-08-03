---
Title: "Shoud we use PHP persistent connections"
Date: 2017-08-03 09:08:55
Categories: [programming]
tags: [php, db]
Authors: sedlav
---

Persistent connections are links that do not close when the execution of your script ends. When a persistent connection is requested, PHP checks if there's already an identical persistent connection (that remained open from earlier) - and if it exists, it uses it. If it does not exist, it creates the link.

[Link](http://us2.php.net/manual/en/features.persistent-connections.php)
