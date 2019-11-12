---
title: Sogou Shurufa Setup
date: 2018-06-27T07:28:47Z
lastmod: 2018-06-27T07:28:47Z
author: Author Name
cover: /img/cover.jpg
categories: ["category1"]
tags: ["tag1", "tag2"]
draft: true
---

Cut out summary from your post content here.

<!--more-->

### Installation

First install the fcitx package. Note if you dont want to spend the next 2hours watching qt4 get compiled, first install the [qtwebkit-bin](https://aur.archlinux.org/packages/qtwebkit-bin/) first. I made this mistake and it took over 2hours for it to finish compiling.

```console
sudo pacman -S fcitx
```
After installing fcitx, install fcitx-sogoupinyin from AUR. This will take sometime so be patient.

```console
yaourt fcitx-sogoupinyin --no-confirm
```
Choose 1-2 to include the elegant skin. This will take 2 Hours if Qt had not been installed before. This package is 21Mb.During installation your screen will display alot of text, don't worry. In-fact have some coffee because its very boring to gaze at.

```console
yaourt qtwebkit-bin --noconfirm
```
The last step is to install the fcitx-im package to have a good experience with Gtk+ and Qt programs.This package is around 35MB.

```console
sudo pacmam -S fcitx-im
```
Finally, a small and important tool to configure fcitx.

```console
sudo pacman -S fcitx-configtool
```

Reboot your machine

```console
sudo reboot
```
### Configuration

When your computer has booted, launch fcitx and on the notification bar, choose Sogou Pinyin as your default input method. To toggle between English and Chinese input, the default setting is Ctrl+Space button.

You are now set to use it.

### Troubleshooting 解决问题

Sometimes I have realised a problem especially when configring fcitx. When you have a problem run fcixt-diagnose and it will
tell you of any problems on your input method.

### Issues am yet to fix

Because of GTK and QT stuff, I dont have a Chinese input when working with the following programs.

* WPS Office
* Spacemacs

Am doing my best to fix the above issues and then I will make an update.

http://tech.memoryimprintstudio.com/issues-with-fcitx-sougou-for-chinese-input-in-emacs/
