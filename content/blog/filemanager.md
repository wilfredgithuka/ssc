+++
author = "Wilfred Githuka"
categories = ["linux"]
date = "2019-01-28"
description = "How to manage files and handle USB Devices"
featured = ""
featuredalt = ""
featuredpath = ""
linktitle = ""
title = "USB Flashdrive, Android Phones Support - This is Thunar"
type = "post"

+++
Lets face it nearly everyone working in an office environment has a flash drive somewhere nearby.
They are the common tools for data transfer in the office environment.

At my workplace, its no different. Sometimes a colleague would hand a flashdrive to copy some document
and if its urgent, I cannot start mounting it on the terminal, thats not efficient.

I need Thunar.

Thunar is a file manager that comes with `XFCE wm`. Its lean and works well for me. Thunar is simple and
lightweight and its functionality can be extended through plug-ins.

We first start by installing it.

`sudo pacman -S thunar thunar-volman udevil udiskie`

That installation includes tools that make it possible to mount large drives. You however need to go 
to settings of `thunar` to make the above work.

Then install tools that help in mounting Android devices as USB disks.

`sudo pacman -S gvfs-mtp gvfs-gphoto2 libmtp`

GVFS is Gnomes virtual file system. The Media Transfer Protocol (MTP) can be used to transfer media files 
to and from many mobile phones (all Windows Phone 7/8/10 devices, most newer Android devices) and media players

However the MPT implementation across different devices is messy, so its not a one-size-fits-all solution.

Reboot and you are good to go.
