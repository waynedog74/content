Title: How to disable Firewalld in CentOS / RHEL / Fedora
Date: 2016-08-26 16:14:26
Category: security
Tags: CentOS, Fedora, FirewallD, RHEL
Slug:how-to-disable-firewalld-in-centos-rhel-fedora
Authors:sedlav
Summary: <p>Type the following command in your console:</p><pre><code>$ sudo systemctl disable firewalld.service</code></pre><br/><p>You can view the servic

<p>Type the following command in your console:</p>
<pre><code>$ sudo systemctl disable firewalld.service</code></pre>
<br/>
<p>You can view the service status with:</p>
<pre><code>$ systemctl status firewalld.service
● firewalld.service - firewalld - dynamic firewall daemon
Loaded: loaded (/usr/lib/systemd/system/firewalld.service; disabled; vendor p
Active: inactive (dead)
Docs: man:firewalld(1)
</code></pre>

