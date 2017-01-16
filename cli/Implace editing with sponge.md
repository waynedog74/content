---
Title: Implace editing with sponge
Date: 2016-11-13 15:31:00
Categories: [cli]
Tags: [sponge, moreutils]
Authors: sedlav
---

**sponge** reads standard input and writes it out to the specified file. Unlike a shell redirect, sponge soaks up all its input before writing the output file. This allows constructing pipelines that read from and write to the same file.

[Link](http://joeyh.name/code/moreutils/)
