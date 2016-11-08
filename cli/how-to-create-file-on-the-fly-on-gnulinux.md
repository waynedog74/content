Title: How to create a  file on the fly on GNU/Linux?
Date: 2016-08-28 00:01:01
Category: cli
Tags: &gt; operator, touch
Slug:how-to-create-file-on-the-fly-on-gnulinux
Authors:sedlav
Summary: You must use the **touch** command or **>** operator, the touch command will create an empty file while **>** also can put content on the file<pre><c

You must use the **touch** command or **>** operator, the touch command will create an empty file while **>** also can put content on the file
<pre><code>touch emptyfile.txt</code></pre>
<br/>
<pre><code>echo -e "This an empty file\nwith a new line" > emptyfile.txt</code></pre>

