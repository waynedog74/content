---
Title: "How to allow root login from one IP address with ssh public keys only"
Date: 2017-07-05 00:33:33
Categories: [security]
tags: [ssh]
Authors: sedlav
---

You can configure OpenSSH for root login from one IP address or subnet only using Match option. The Match option act as a conditional block. If all of the given conditions are satisfied, OpenSSH can override global section config file. You can limit or grant access to sshd features with the Match option.

[Link](https://www.cyberciti.biz/faq/match-address-sshd_config-allow-root-loginfrom-one_ip_address-on-linux-unix/)
