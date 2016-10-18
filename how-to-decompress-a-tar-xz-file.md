Title: How to decompress a tar.xz file?
Date: 2016-08-30 02:26:33
Category: Tips
Tags: tar
Slug:how-to-decompress-a-tar-xz-file
Authors:sedlav
Summary: You must use the tar tool with J option<pre><code>$ tar xJvf php-7.0.10.tar.xz</code></pre>x = extractf = filev = verboseJ = Filter the archive t

You must use the tar tool with J option
<pre><code>$ tar xJvf php-7.0.10.tar.xz</code></pre>
x = extract
f = file
v = verbose
J = Filter the archive through xz

