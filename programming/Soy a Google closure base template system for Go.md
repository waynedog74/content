---
Title: "Soy a Google Closure templates base system for Go"
Date: 2017-09-13 15:27:14
Categories: [programming]
tags: [go, soy]
Authors: sedlav
---

Package soy is an implementation of Google's Closure Templates, which are data-driven templates for generating HTML.

Compared to html/template, Closure Templates have a few advantages

* Intuitive templating language that supports simple control flow, expressions and arithmetic.
* The same templates may be used from Go, Java, and Javascript.
* Internationalization is built in
* High performance (> 3x faster than html/template in BenchmarkSimpleTemplate)
* Hot reload for templates
* Parse a directory tree of templates

[Link](https://godoc.org/github.com/robfig/soy)
