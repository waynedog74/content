---
Title: "Correct Index Choices for Equality + LIKE Query Optimization"
Date: 2017-04-11 16:30:40
Categories: [data base]
Tags: [mysql, mariadb, percona]
Slug: correct-index-choices-for-equality-like-query-optimization/
Authors: sedlav
---

> As part of our support services, we do a lot of query optimization. This is where most performance gains come from. Here’s an example of the work we do.

> Some days ago a customer arrived with the following table:

```sql
CREATE TABLE `infamous_table` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `member_id` int(11) NOT NULL DEFAULT '0',
  `email` varchar(200) NOT NULL DEFAULT '',
  `msg_type` varchar(255) NOT NULL DEFAULT '',
  `t2send` int(11) NOT NULL DEFAULT '0',
  `flag` char(1) NOT NULL DEFAULT '',
  `sent` varchar(100) NOT NULL DEFAULT '',
  PRIMARY KEY (`id`),
  KEY `f` (`flag`),
  KEY `email` (`email`),
  KEY `msg_type` (`msg_type`(5)),
  KEY `t_msg` (`t2send`,`msg_type`(5))
) ENGINE=InnoDB DEFAULT CHARSET=latin1
```

[Link](https://www.percona.com/blog/2017/04/11/correct-index-choices-for-equality-like-query-optimization/)
