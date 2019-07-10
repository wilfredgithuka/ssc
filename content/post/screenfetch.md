---
title: Screenfetch - 显示系统详细信息
date: 2018-07-20T17:48:48+03:00
lastmod: 2018-07-20T17:48:48+03:00
author: Wilfred Githuka 楚大洋
cover: https://dominicm.com/wp-content/uploads/2016/03/screenfetch-arch-linux.png
categories: ["Unix/Linux操作系统"]
tags: ["screenfetch", "系统详细信息"]
draft: false
---
![image](https://dominicm.com/wp-content/uploads/2016/03/screenfetch-arch-linux.png)

screenFetch是一个Bash屏幕截图信息工具，可在执行时打印ASCII艺术以及基本系统信息。 
包括Arch Linux在内的许多发行版都支持独特的ASCII艺术。
在登录时自动运行它以立即查看系统信息非常有用。

<!--more-->

安装screenfetch有两个方法．你可以让它启动的时候，先显示系统详细信息或者你打开Bash的时候显示
系统详细信息．

## 安装
```console
sudo pacman -Syu screenfetch
```

打开Bash的设置文件

```console
sudo nano ~/.bashrc
```
在打开Bash看看结果怎么样.

Enjoy :-)

## References

* [Dominic](https://www.dominicm.com)