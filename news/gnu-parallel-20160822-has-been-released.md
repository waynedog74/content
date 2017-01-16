---
Title: "GNU Parallel 20160822 has been released."
Date: 2016-08-22 14:26:40
Categories: [news]
Tags: [GNU Parallel]
Slug: gnu-parallel-20160822-has-been-released
Authors: sedlav
---

GNU Parallel 20160822 ('Og Nomekop') has been released. It is available for [download](http://ftpmirror.gnu.org/parallel/)

**Hightlights**

* --tmuxpane opens jobs in panes in tmux. Useful if you want to monitor progress of less than 100 simultaneous jobs.
* --linebuffer now treats \r as line ending, too.
* Perl changes forces use of floats to be given with leading zero, so 0.1 and not .1
* --xapply renamed to --link.
* Support for pdksh will fade until someone packages it for Ubuntu 16.

GNU Parallel is a shell tool for executing jobs in parallel using one or more computers. A job can be a single command or a small script that has to be run for each of the lines in the input.

[Link](http://savannah.gnu.org/forum/forum.php?forum_id=8658)
