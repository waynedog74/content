---
Title: "Introducing Faktory"
Date: 2017-11-20 18:46:25
Categories: [devops]
Tags: [faktory, jobs server]
Authors: sedlav
---

At a high level, Faktory is a work server. It is the repository for background jobs within your application. Jobs have a type and a set of arguments and are placed into queues for workers to fetch and execute.

You can use this server to distribute jobs to one or hundreds of machines. Jobs can be executed with any language by clients using the Faktory API to fetch a job from a queue.

[Link](https://github.com/contribsys/faktory)
