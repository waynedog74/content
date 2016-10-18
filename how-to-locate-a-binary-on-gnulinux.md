Title: How to locate a binary on GNU/Linux?
Date: 2016-08-23 19:19:19
Category: Tips
Tags: whereis
Slug:how-to-locate-a-binary-on-gnulinux
Authors:sedlav
Summary: You must use the **whereis** command:<pre><code>$ whereis git/usr/bin/git /usr/bin/X11/git /usr/local/bin/git</code></pre><p>**whereis** - loca

You must use the **whereis** command:
<pre>
<code>$ whereis git
/usr/bin/git /usr/bin/X11/git /usr/local/bin/git
</code>
</pre>
<p>
**whereis** - locate the binary, source, and manual page files for a command</p>

