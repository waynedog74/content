---
Title: Fossil is a simple, high-reliability, distributed software configuration management system
Date: 2016-09-08 21:02:58
Categories: [vcs]
tags: [fossil]
Slug: fossil-is-a-simple-high-reliability-distributed-software-configuration-management-system
Authors: sedlav
---

**Fossil** is a simple, high-reliability, distributed software configuration management system with these advanced features:

* Integrated Bug Tracking, Wiki, and Technotes - In addition to doing distributed version control like Git and Mercurial, Fossil also supports bug tracking, wiki, and technotes.
* Built-in Web Interface - Fossil has a built-in and intuitive web interface with a rich assortment of information pages (examples) designed to promote situational awareness.
* Self-Contained - Fossil is a single self-contained stand-alone executable. To install, simply download a precompiled binary for Linux, Mac, OpenBSD, or Windows and put it on your $PATH. Easy-to-compile source code is also available.
* Simple Networking - No custom protocols or TCP ports. Fossil uses ordinary HTTP (or HTTPS or SSH) for network communications, so it works fine from behind restrictive firewalls, including proxies. The protocol is bandwidth efficient to the point that Fossil can be used comfortably over dial-up.
* CGI/SCGI Enabled - No server is required, but if you want to set one up, Fossil supports four easy server configurations.
* Autosync - Fossil supports "autosync" mode which helps to keep projects moving forward by reducing the amount of needless forking and merging often associated with distributed projects.
* Robust & Reliable - Fossil stores content using an enduring file format in an SQLite database so that transactions are atomic even if interrupted by a power loss or system crash. Automatic self-checks verify that all aspects of the repository are consistent prior to each commit.
* Free and Open-Source - Uses the 2-clause BSD license.

[Link](https://www.fossil-scm.org/)
