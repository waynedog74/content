Title: How to get the full path of a command on GNU/Linux?
Date: 2016-09-01 03:30:26
Category: cli
Tags: which
Slug:how-to-get-the-full-path-of-a-command-on-gnulinux
Authors:sedlav
Summary: You must use the **which** command:<pre><code>$ which lsalias ls='ls --quoting-style=literal --color'/usr/bin/ls</code></pre>

You must use the **which** command:
<pre><code>$ which ls
alias ls='ls --quoting-style=literal --color'
/usr/bin/ls
</code></pre>

