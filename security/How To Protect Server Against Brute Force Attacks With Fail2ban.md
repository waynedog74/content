---
Title: "How To Protect Server Against Brute Force Attacks With Fail2ban"
Date: 2017-11-09 10:46:24
Categories: [security]
tags: [fail2ban, ids]
Authors: sedlav
---

**Fail2ban** is an intrusion prevention software, framework which protect server against brute force attacks. It’s Written in Python programming language. Fail2ban work based on auth log files, by default it will scan the auth log files such as /var/log/auth.log, /var/log/apache/access.log, etc.. and bans IPs that show the malicious signs, too many password failures, seeking for exploits, etc.

[Link](https://www.2daygeek.com/how-to-install-setup-configure-fail2ban-on-linux/)
