---
title: How to Install Darktable 3.0.0 in Ubuntu 18.04, 19.10 
date: 2019-12-25 14:01:32
categories: [media]
tags: [darktable]
authors: sedlav
---

How to Install Darktable 3.0.0 in Ubuntu 18.04, 19.10 | UbuntuHandbook

 UbuntuHandbook

News, Tutorials, Howtos for Ubuntu Linux

 How to Install Darktable 3.0.0 in Ubuntu 18.04, 19.10 December 24, 2019 — Leave a comment Darktable RAW image editor 3.0 was released today with new major updates. Here’s how to install it in Ubuntu 18.04, Ubuntu 19.04, and Ubuntu 19.10.

Darktable 3.0 comes with a complete rework of the user interface. The GUI now is fully controlled by GTK+ CSS rules, which makes the whole GUI themable. And this version comes with several different themes.

Other changes in the release include:

8. New shortcuts to collapse borders, sidebars, histogram and navigation modules, allowing a new borderless editing experience.
9. Undo/redo support in lighttable for tags, color labels, metadata, etc.
10. A new timeline view in the lighttable.
11. A new ‘culling’ mode added to the lightable view.
12. Improved support for 4K and 5K monitors.
13. Support for exporting to Google Photos
14. More camera support, white balance presets, and noise profiles
15. See the full changes in the github.
How to Install Darktable 3.0 in Ubuntu: The darktable release PPA seems no longer being updated. I’ve uploaded the 3.0 packages into the unofficial PPA for 64-bit Ubuntu 18.04, Ubuntu 19.04, Ubuntu 19.10.

1\. Open terminal (Ctrl+Alt+T) and run command to add the PPA:

```
sudo add-apt-repository ppa:ubuntuhandbook1/darktable
```

Type user password (no asterisk feedback) for sudo prompts and hit Enter to continue.

2\. If an old version was installed, upgrade it using Software Updater:

or run commands in terminal to install Darktable:

```
sudo apt update

sudo apt install darktable
```

Uninstall: To remove the PPA, either launch Software & Updates and navigate to Other Software, or run command in terminal:

```
sudo add-apt-repository --remove ppa:ubuntuhandbook1/darktable
```

To remove the RAW image editor, use Ubuntu Software.

 Ji m  I'm a freelance blogger who started using Ubuntu 5+ years ago and wishes to share my experiences and some useful tips with Ubuntu beginners and lovers. Please notify me if you find any typo/grammar/language mistakes. English is not my native language. Contact me on Google Plus or email to ubuntuhandbook1@gmail.com 30. How to Install The Latest...
 Leave a Reply Cancel reply Comment

Text formatting is available via select HTML.

```
<a href="" title=""> <abbr title=""> <acronym title=""> <b> <blockquote cite=""> <cite> <code> <del datetime=""> <em> <i> <q cite=""> <s> <strike> <strong> 
```

Name \*

Email \*

Website

 Current ye@r \*

 Leave this field empty

[Link](http://ubuntuhandbook.org/index.php/2019/12/install-darktable-3-0-0-ubuntu-18-04-19-10/)
