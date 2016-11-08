Title: Find files and perform an action on them
Date: 2016-08-13 22:23:20
Category: cli
Tags: find, while
Slug:find-files-and-perform-an-action-on-them
Authors:sedlav
Summary: <pre>$ find DIR -name filename -type f -print0  | while read -d $'\0' file; do echo $file; done</pre>

<pre>$ find DIR -name filename -type f -print0  | while read -d $'\0' file; do echo $file; done</pre>

