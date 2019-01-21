+++
author = "Wilfred Githuka"
categories = ["linux, emacs"]
date = "2019-01-18"
description = "How to Add Chinese Input In Spacemacs on an Archlinux Machine"
featured = ""
featuredalt = ""
featuredpath = ""
linktitle = ""
title = "Chinese Input in Emacs on Linux - Attempt 1"
type = "post"

+++
Since this year started my Chinese documentation has suffered alot since I don't have Chinese input in Emacs.
I use spacemacs as my primary text editor and really need Chinese input. 

Fcitx(Flexible Input Method Framework) currently works with the other apps together with Sogou input 
but not emacs. I seek to find out why. Running fcitx-diagnose says all is okay except for:

* Config GUI for gtk2: **Config GUI for gtk2 not found.**
* Config GUI for kde: **`kcmshell4` not found.**

I have tried to install the above components but still no effect.

First lets learn abit how fcitx works...

## For Non Desktop Environment

Add the following lines to your desktop start up script files to register the input method modules and support xim programs.

Use .xprofile if you are using KDM, GDM, LightDM or SDDM.

Use .xinitrc if you are using startx or Slim.

* export GTK_IM_MODULE=fcitx
* export QT_IM_MODULE=fcitx
* export XMODIFIERS=@im=fcitx

Re-login to make these environment changes effective.

If your LC_CTYPE is English, you may not be able to use input method in emacs due to an old emacs' bug. 
You can set your LC_CTYPE to something else such as zh_CN.UTF-8 before emacs starts to get rid of this problem.

Note that the corresponding locale should be enabled on your your system. Uncomment the corresponding line, for example, 
zh_CN.UTF-8, in /etc/locale.gen and run locale-gen.

## Emacs

If your LC_CTYPE is English, you may not be able to use input method in emacs due to an old emacs bug. You can set your 
LC_CTYPE to something else such as zh_CN.UTF-8 before emacs starts to get rid of this problem.

Note that the corresponding locale should be generated on your your system.

The default fontset will use `-*-*-*-r-normal--14-*-*-*-*-*-*-*' as basefont (in src/xfns.c), 
if you do not have one matched (like terminus or 75dpi things, you can look the output of `xlsfonts'), 
XIM can not be activated.

## Another Method

安装fcitx输入法，在 ~/.xinitrc文件中添加如下内容 (我用startx启动图形环境，所以在~/.xinitrc中配置X会话)

* export LC_CTYPE="zh_CN.UTF-8"
* export XMODIFIERS='@im=fcitx'
* export GTK_IM_MODULE=xim
* export QT_IM_MODULE=xim
* export GTK3_IM_MODULE=xim
* fcitx -d

## References

* [Memory Imprint Studio](http://tech.memoryimprintstudio.com/issues-with-fcitx-sougou-for-chinese-input-in-emacs/)
* [Archlinux Wiki Fcitx](https://wiki.archlinux.org/index.php/Fcitx#Ctrl+Space_fail_to_work_in_GTK_programs)
* [Emacs Use Fcitx](https://www.cnblogs.com/jiqingwu/p/emacs_use_fcitx.html)
