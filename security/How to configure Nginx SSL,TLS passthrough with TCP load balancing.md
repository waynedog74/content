---
Title: "How to configure Nginx SSL/TLS passthrough with TCP load balancing"
Date: 2017-06-07 22:51:47
Categories: [security]
Tags: [ssl, tls, nginx]
Slug: configure-nginx-ssltls-passthru-with-tcp-load-balancing
Authors: sedlav
---

Usually, SSL termination takes place at the load balancer and unencrypted traffic sent to the backend web servers. All HTTPS/SSL/TLS and HTTP requests are terminated on the Nginx server itself. Nginx server uses the HTTP protocol to speak with the backend server. You must take great care to make sure no one snoops traffic between your private network.

[Link](https://www.cyberciti.biz/faq/configure-nginx-ssltls-passthru-with-tcp-load-balancing)
