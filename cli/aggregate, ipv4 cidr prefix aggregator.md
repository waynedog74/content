---
Title: aggregate, ipv4 cidr prefix aggregator
Date: 2018-01-29 11:39:47
Categories: [cli]
tags: [aggregate, debian]
Authors: sedlav
---

aggregate takes a list of prefixes in conventional format on stdin, and performs two optimisations to reduce the length of the prefix list. It removes any supplied prefixes which are supurfluous because they are already included in another supplied prefix (e.g., 203.97.2.0/24 would be removed if 203.97.0.0/17 was also supplied), and identifies adjacent prefixes that can be combined under a single, shorter-length prefix (e.g., 203.97.2.0/24 and 203.97.3.0/24 can be combined into the single prefix 203.97.2.0/23).

[Link](https://packages.debian.org/stretch/aggregate)
