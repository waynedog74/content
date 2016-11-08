Title: How to disable SELinux in CentOS / RHEL / Fedora
Date: 2016-08-26 04:12:11
Category: security
Tags: CentOS, Fedora, RHEL, SELinux
Slug:how-to-disable-selinux-in-centos-rhel-fedora
Authors:sedlav
Summary: You must edit the /etc/sysconfig/selinux file and set SELINUX=disabled<pre><code>$ cat /etc/sysconfig/selinux# This file controls the state of SELin

You must edit the /etc/sysconfig/selinux file and set SELINUX=disabled
<pre><code>$ cat /etc/sysconfig/selinux
# This file controls the state of SELinux on the system.
# SELINUX= can take one of these three values:
#     enforcing - SELinux security policy is enforced.
#     permissive - SELinux prints warnings instead of enforcing.
#     disabled - No SELinux policy is loaded.
SELINUX=disabled
# SELINUXTYPE= can take one of these three values:
#     targeted - Targeted processes are protected,
#     minimum - Modification of targeted policy. Only selected processes are protected. 
#     mls - Multi Level Security protection.
SELINUXTYPE=targeted
</code></pre>

