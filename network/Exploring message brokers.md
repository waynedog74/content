---
Title: "Exploring message brokers"
Date: 2016-12-13 09:11:00
Categories: [network]
Tags: [RabbitMQ, Kafka, ActiveMQ, Kestrel]
Authors: sedlav
---

> Some time ago, I was asked by one of our customer to review a selection of OSS message brokers and propose a couple of good candidates. The requirements were fairly simple: behave well when there’s a large backlog of messages, be able to create a cluster and in case of the failure of a node in a cluster, try to protect the data but never blocks the publishers even though that might imply data lost.

[Link](https://www.percona.com/blog/2014/05/05/exploring-message-brokers/)
