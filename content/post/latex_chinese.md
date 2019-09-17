---
title: Finally I Got Spacemacs+LaTeX+搜狗输入法 Working 成功了！
date: 2018-08-16T10:15:37+03:00
lastmod: 2018-08-27T10:15:37+03:00
author: Wilfred Githuka 楚大洋
cover: /img/kisii-evening.jpg
categories: ["LaTeX"]
tags: ["spacemacs"]
draft: false
---

After weeks and weeks of toiling on the terminal, I finally finished a piece
of my Linux workflow. I managed to have Chinese Characters input using
搜狗输入法 to work in Spacemacs and have the same output in LaTeX. 

<!--more-->
This was not easy to say the least, due to poorly written documentation on the above workflow.

To save you the time of having to bang your head trying to install the above, 
this post will guide you on what to install and have success like me.

## 我的系统的状态　My System
* OS:Archlinux
* Tool:Spacemacs
* Input Method:搜狗输入法
* Fonts:Basic Chinese Fonts

## 安装　Installation
### 字型Fonts
In order for you to have Chinese input you need some basic fonts installed
into your system. I recomend the fonts available on the Archlinux Fonts page
under the category:Chinese. This is available [here](https://wiki.archlinux.org/index.php/fonts#Chinese). Install:

* adobe source han fonts
* noto Chinese fonts

### 搜狗输入法Sougou Input Method
Sogou input method is the defacto Chinese input method available in China. Its
quite popular and I like it. I have done an extensive post on how to install
it on your linux machine. Check it out here.

### X显示服务器设置XServer Settings
This is a crucial step that needs to be performed in order to solve the GTK and
Qt environments for linux applications. Add the following to your .xprofile (ignore the bullets)

* export GTK_IM_MODULE=fcitx
* export QT_IM_MODULE=fcitx
* export XMODIFIERS=@im=fcitx

Save and reboot.

### Spacemacs
Spacemacs is very cool and can be installed from this [Github repo](https://github.com/syl20bnr/spacemacs) which explains the whole process neatly.

### Spacemacs LaTeX Layer
By now you should be having Chinese input working inside spacemacs. That is
something good. We now need to have LaTeX installed on Spacemacs. This can
simply be done by following this [page](https://github.com/syl20bnr/spacemacs/tree/master/layers/%2Blang/latex#install).

A build command can be specified via the layer variable latex-build-command.

If LatexMk is specified, the appropriate LatexMk configuration will be applied. (the default on systems with latexmk in the path) This variable can be set to any of the entities in TeX-command-list, including any custom entries you may have added there. To use the regular AucTeX command set latex-build-command to LaTeX as shown below.

dotspacemacs-configuration-layers '(
  (latex :variables latex-build-command "LaTeX"))

And also enable autofill.

dotspacemacs-configuration-layers '(
  (latex :variables latex-enable-auto-fill t))

### Chinese Input on LaTeX
To enable Chinese characters rendering on LaTeX you need to have the following
added to the document. Put all your chinese content within the begin and end CJKutf8 commands.(ignore the bullets)

* \usepackage{CJKutf8}
* \begin{document}
* \begin{CJK*}{UTF8}{gbsn}
* .
* .
* \end{CJK*}

Save and reboot

When you build your pdf output, you should see the Chinese characters rendered
at the output nicelly.

I wrote my work report using LaTeX and its beautiful :-)
