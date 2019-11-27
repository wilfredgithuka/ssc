---
title: "安装中文输入法在 Archlinux+i3 系统"
date: 2019-11-26T20:19:26+03:00
draft: false
---
* 本文作者：楚大洋
* 本文链接：https://chinese.githuka.com
* 本文大小： 40kB
* 发表于：26号11月2019年
* 更新于：26号11月2019年
* 分类于：安装, 字形，fcitx
* 字数：100字
* 版权声明：本博客所有文章除特别声明外，均采用 BY-NC-SA 许可协议。转载请注明出处！

终于我能使用中文输入法在我的电脑上。本说明书是为了你能使用一个中文输入法在 Archlinux 那种的系统。在普通的 Linux 系统有好多的专门中文输入法软件，可是如果本系统有 i3 的专门管理系统，你还是要找其他的中文输入法软件。

## 安装相关的软件

首先你要安装 fcitx (Flexible Input Method Framework) ──即小企鹅输入法，它是一个以 GPL 方式发布的输入法平台,可以通过安装引擎支持多种输入法，支持简入繁出，是在 Linux 操作系统中常用的中文输入法。fcitx 还有其他的工具需要一起安装。按照以下的方式就好了。

```
sudo pacman -S fcitx fcitx-sunpinyin fcitx-im fcitx-configtool
```
## 安装中文字形

```
sudo pacman -S sudo pacman -S adobe-source-han-sans-cn-fonts adobe-source-han-sans-tw-fonts adobe-source-han-serif-cn-fonts adobe-source-han-serif-tw-fonts wqy-microhei wqy-zenhei opendesktop-fonts
```

## 设置

如果 fcitx 没有自动启动，请将 fcitx & 加入 ~/.xinitrc. 把以下的内容也加入在 ~/.xinitrc

```
GTK_IM_MODULE=fcitx
QT_IM_MODULE=fcitx
XMODIFIERS=@im=fcitx
```

如果你碰到一个问题， 你可以执行以下的命令。fcitx 会告诉你问题在那里.

```
fcitx diagnose
```
