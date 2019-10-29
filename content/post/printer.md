---
title: Printer
date: 2018-08-31T07:46:19+03:00
lastmod: 2018-08-31T07:46:19+03:00
author: Author Name
cover: /img/cover.jpg
categories: ["category1"]
tags: ["tag1", "tag2"]
draft: true
---

Cut out summary from your post content here.

<!--more-->

To use cups-pdf, restart cups and visit the cups
web interface at http://localhost:631/

You can now add a "Virtual Printer (PDF Printer)"
and use the Postscript/Generic postscript color
printer driver.

Note that cups-pdf has a configuration
file in /etc/cups. The default location for
pdf output is /var/spool/cups-pdf/$username.

## Enable and start org.cups.cupsd.service.

sudo systemctl enable org.cups.cupsd.service
sudo systemctl start  org.cups.cupsd.service


The remaining content of your post.
