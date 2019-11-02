---
title: Vagrant is stuck. Authentication failure. Retrying
date: 2019-10-29 16:50:35
categories: [devops]
tags: [vagrant]
authors: sedlav
---

**Problem**

When running "vagrant up" to bring up a Vagrant Virtualbox, it can't authenticate.  It's retries forever and eventually gives up: `default: Warning: Authentication failure. Retrying...`

**Solution**

You can unstick the vagrant machine, but it involves some careful copying and pasting. Find the IdentityFile vagrant is using...

[Link](https://openedx.atlassian.net/wiki/spaces/OXA/pages/157802739/Vagrant+is+stuck+Authentication+failure.+Retrying...)
