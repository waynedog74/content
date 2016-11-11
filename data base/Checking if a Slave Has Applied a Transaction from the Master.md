Title: Checking if a Slave Has Applied a Transaction from the Master
Date: 11-10-2016 15:50
Category: data base
Tags: percona, mysql, mariadb
Authors:sedlav
Summary: In this blog post, we will discuss how we can verify if an application transaction executed on the master has been applied to the slaves

> In this blog post, we will discuss how we can verify if an application transaction executed on the master has been applied to the slaves... One way to do this is using a built-in function called MASTER_POS_WAIT. This function receives a binary log name and position. It will block the query until the slave applies transactions up to that point, or timeout.

[Link](https://www.percona.com/blog/2016/11/08/checking-if-slave-has-applied-a-transaction/)
