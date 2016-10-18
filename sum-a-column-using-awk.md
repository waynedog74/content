Title: Sum a column using awk
Date: 2016-08-09 20:30:44
Category: Command Fu
Tags: awk
Slug:sum-a-column-using-awk
Authors:sedlav
Summary: <pre><code>$ cat stat.txtJan  124Feb  929Mar  708Apr  947</code></pre><pre><code>$ awk '{ SUM += $2} END { print SUM }' stat.txt</code></pre>Re

<pre><code>$ cat stat.txt
Jan  124
Feb  929
Mar  708
Apr  947
</code></pre>
<pre><code>$ awk '{ SUM += $2} END { print SUM }' stat.txt</code></pre>
Result = 2708

