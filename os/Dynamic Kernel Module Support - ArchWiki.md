---
title: Dynamic Kernel Module Support - ArchWiki
date: 2021-07-22 15:48:38
categories: [os]
tags: [linux,dkms]
authors: sedlav
---

Dynamic Kernel Module Support (DKMS) is a program/framework that enables generating Linux kernel modules whose sources generally reside outside the kernel source tree. The concept is to have DKMS modules automatically rebuilt when a new kernel is installed.This means that a user does not have to wait for a company, project, or package maintainer to release a new version of the module. Since the introduction of pacman hooks, the rebuild of the modules is handled automatically when a kernel is upgraded.

[Link](https://wiki.archlinux.org/title/Dynamic_Kernel_Module_Support)
