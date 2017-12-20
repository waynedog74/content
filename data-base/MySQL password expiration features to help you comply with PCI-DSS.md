---
Title: "MySQL password expiration features to help you comply with PCI-DSS"
Date: 2017-12-20 10:50:52
Categories: [data base]
tags: [mysql, mariadb, percona]
Authors: sedlav
---

MySQL passwordPCI Compliance (section 8.2.4) requires users to change password every 90 days. Until MySQL 5.6.6 there wasn’t a built-in way to comply with this requirement.

Since MySQL version 5.6.6 there’s a password_expired feature which allows to set a user’s password as expired.
This has been added to the mysql.user table and its default value it’s “N.” You can change it to “Y” using the

ALTER USER

 statement.


[Link](https://www.percona.com/blog/2016/02/04/mysql-password-expiration-features-help-comply-pci-dss/)
