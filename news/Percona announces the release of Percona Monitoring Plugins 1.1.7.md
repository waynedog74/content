---
Title: "Percona announces the release of Percona Monitoring Plugins 1.1.7"
Date: 2016-12-10 12:41:00
Categories: [news]
tags: [percona]
Authors: sedlav
---

Percona announces the release of Percona Monitoring Plugins 1.1.7.

Changelog:

* New Nagios script pmp-check-mongo.py for MongoDB.
* Added MySQL socket and flag options to Cacti PHP script.
* Added disk volume check on “Mounted on” in addition to “Filesystem” to Cacti PHP script to allow monitoring of tmpfs mounts.
* Allow delayed slave to have SQL thread stopped on pmp-check-mysql-replication-delay check.
* Fix for –unconfigured flag of pmp-check-mysql-replication-delay.
* Fix for max_duration check of pmp-check-mysql-innodb when system and MySQL timezones mismatch.
* Fix rare nrpe broken pipe error on pmp-check-unix-memory check.
* Updated package spec files.

[Link](https://www.percona.com/blog/2016/12/09/percona-monitoring-plugins-1-1-7-release/)
