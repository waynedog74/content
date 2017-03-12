---
Title: "SSH Agent Forwarding considered harmful"
Date: 2017-03-11 14:47:24
Categories: [security]
tags: [ssh]
Authors: sedlav
---

SSH Agent Forwarding can be enabled by calling ssh -A or by setting the AgentForward flag in your config. It is meant as an easy way to connect to a host A with your SSH key and from there connect to another host B with that same key. This obviously is only needed if you cannot connect to host B directly from your workstation.

[Link](https://heipei.github.io/2015/02/26/SSH-Agent-Forwarding-considered-harmful/lin)
