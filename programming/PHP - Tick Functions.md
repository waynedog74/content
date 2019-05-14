---
title: PHP - Tick Functions
date: 2019-05-14 18:41:01
categories: [programming]
tags: [php]
authors: sedlav
---

Ticks provide simulated background processing within PHP.

OverviewTicks were added to PHP 4.0.3 as a way to simulate background processing for blocks of code. They allow one or more functions to be called as a side effect of having expressions evaluated. Simply put, developers can set up functions that are called automatically as the script runs - this is useful for running functions that perform status checking, cleanup, notification, and so on. Ticks can also be indispensable for quick and dirty debugging - see the simple example below.

[Link](http://www.phpdig.net/ref/rn62.html)
