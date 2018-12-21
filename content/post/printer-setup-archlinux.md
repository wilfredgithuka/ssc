---
title: Printer Setup Archlinux
date: 2018-06-27T07:20:56Z
lastmod: 2018-06-27T07:20:56Z
author: Author Name
cover: /img/cover.jpg
categories: ["category1"]
tags: ["tag1", "tag2"]
draft: true
---

Printer setup is not an easy thing in Archlinux. Apart from installing the CUPS package, one needs to dig deeper into the system to make the printing process successful.

<!--more-->

### Introduction

Office printers are networked which makes it abit more complex. On Windows, I just had to click on Printer settings, install some drivers then the printer would submissively print a test page to confirm a successful connection.

The CUPS web interface can be accessed by {https://localhost:631/admin}

### Identify the Printers
This is the forst step to know what type and model of printers that I was configuring. 

### Adding Yourself To The lp Group & CUPS Web Interface Needs A Password
After adding myself to the lp group, CUPS was still requiring a password. This issue took a while but I finally found an answer, first from [Will Halley]{https://willhaley.com/blog/printing-in-arch-linux/} and then a more detailed explanation from the [Archlinux Forums]{https://bbs.archlinux.org/viewtopic.php?pid=376974#p376974}.

```console
sudo groupadd printadmin
sudo usermod -a -G printadmin $USER
```
Then edit /etc/cups/cups-files.conf and add printadmin while removing sys

```console
SystemGroup printadmin root
```

Save and reboot. After rebooting, access the CUPS web interface and log in.

### PPD Files
PPD are the drivers for the printers in the Linux world. You can google the required PPDs for whatever printer you have in your office. After the correct PPDs are installed, the printer will work well.

And that is how printers are installed in Archlinux :-)

