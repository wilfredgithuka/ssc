---
title: "Printer Configuration in Archlinux"
date: 2019-05-06T15:58:26Z
draft: false
---

Printing on Archlinux or generally Linux is not easy. Thus manual is a
guide on how to achieve printing on Archlinux.

Note that I highly recommend the [Archlinux Wiki](https://wiki.archlinux.org) which is more deep and explains the concepts better. My guide shall achieve the same results but faster.

## Installation

Install the required packages for printing. CUPS is the standards-based, open source printing system developed by Apple Inc. for macOS® and other UNIX®-like operating systems.

```
sudo pacman -S cups cups-pdf hplip libcups system-config-printer
```

## Permissions

Add yourself to the **lpadmin** group to access the printing service.

```
sudo groupadd lpadmin
sudo usermod -aG lpadmin username
```

## Config

Edit the /etc/cups/cups-files.conf and add the **SystemGroup** line.

```
sudo nano /etc/cups/cups-files.conf

SystemGroup sys root lpadmin
```

## CUPS Service

Start the CUPS service. CUPS provides a org.cups.cupsd.socket unit. If org.cups.cupsd.socket is enabled (and org.cups.cupsd.service is disabled), systemd will not start CUPS immediately, it will just listen to the appropriate sockets.

Then, whenever a program attempts to connect to one of these CUPS sockets, systemd will start org.cups.cupsd.service and transparently hand over control of these ports to the CUPS process.

This way, CUPS is only started once a program wants to make use of the service.

```
sudo systemctl enable org.cups.cupsd.service
```
Reboot your machine for the changes to take place.

## Usage

Afer rebooting launch **system-config-printer** from the terminal, then
enter your username and password.

## References

* [Jonas Tech Notebook](https://gorauskas.org/linux/arch/ArchPrintingSetup)
* [Archlinux Wiki](https://wiki.archlinux.org/index.php/CUPS#Installation)
