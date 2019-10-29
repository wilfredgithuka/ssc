---
title: "Intergrating Linux In My Chinese Workflow"
date: 2018-06-05T10:36:21Z
draft: false
---
![image](/img/archlinux.png)

<center><h3>[中文版](#中文版)</h1></center>

According to [statscounter](https://gs.statscounter.com/os-version-market-share/windows/desktop/china), 54% of desktops in China run Windows 7 while 27% run Windows10. Windows 7 has long been a favourite of the masses due to its usability and security. If fuses well with Chinese software.

Back in 2014 during my time in Nanjing, China I tried to swich to Linux as my primary OS but the change was too quick, and many of the Windows applications had not Linux alternatives, so within 2 weeks, I reverted back to Windows.
My Chinese work environment is very busy. So Recently, I have started to intergrate Linux into my workflow. This involves gradual change as I move to Linux completely within 2 months time. I must admit that there will be some tough times but its worth it. 

So why am I changing to Linux?

* Improved hardware performance - Windows is too heavy and bloated which is making my hardware work too much.
* Hardware Intergration - I can configure/integrate  all my devices well on Linux
* Learn Linux More - I have been using Linux full time since 2015. I think I am ready
* Easy To Tweak & Configure - In Linux everything is a file. There is no dreaded System Registry.
* OpenSource - I need know whats happening in the background and am also aware of my security more.
* Learn Chinese - This will also be a good opportunity to improve my Chinese since I will be reading Chinese forums

This document is my tracking pad for my progress. My distro is Archlinux.

### Linux Installation

I use Archlinux which I have installed on a persistent 1TB USB external drive. I did this so that I can have my Windows intact as I slowly move away from it. To use Archlinux, I simply reboot while hitting F12 key and select Archlinux. When I need to do a presentation, I just reboot back to Windows.

I plan to do this until Mid June 2018 when I will completely remove Windows as my primary OS and put Archlinux. Its a slow move and I want to make sure that I get the required tools. Its weired to start writing commands when showing your boss a new idea.

### Required Tools And Applications

When moving to Linux, the following are the apps that I use which work like their windows counterparts and even better.

* Chinese Fonts
* Sogou Input Method
* Office Suite
* PDF Renders
* WeChat Desktop
* WhatsApp
* QQ Desktop
* Disk Management
* CompressedFiles


### Disk Management

When moving to Linux from a Windows environment, one of the challenges that you may experience is the urge to check on your disks once in a while. To do this you can simply mount your Windows formated disks from Linux. Preety easy? Huh?
Not really. They will be mounted as Read-Only. Install ntfs-3g package to remove the read-only lock

#### Installation

```console
sudo pacman -S ntfs-3g
```
Once it install, you can mount your NTFS formated disks easily.

If you have any questions regarding the above steps, just write
your comments in the comments section below :-)

# 中文版

回到2014年，我在中国南京的时候，我尝试将Linux作为我的主要操作系统，但这种变化太快了，许多Windows应用程序都没有Linux替代品，所以在2周内，我又恢复到了Windows。
我的中国工作环境非常繁忙。所以最近，我开始将Linux整合到我的工作流程中。这涉及到在2个月内完全迁移到Linux时的逐渐变化。我必须承认，会有一些艰难的时刻，但它值得。

那么，为什么我要更改为Linux？

* 改进的硬件性能 - Windows太重且太臃肿，这使我的硬件工作太多。
* 硬件集成 - 我可以在Linux上很好地配置/集成所有设备
* 了解更多Linux - 自2015年以来，我一直在使用Linux。我认为我已经做好准备
* 轻松调整和配置 - 在Linux中，一切都是一个文件。没有可怕的系统注册表。
* 开源 - 我需要知道在后台发生了什么，我也更多地意识到我的安全。
* 学习中文 - 这将是一个很好的机会来提高我的中文水平，因为我将阅读中文论坛

这个文件是我的进步跟踪板。我的发行版是Archlinux。

### Linux安装

我使用安装在持续1TB USB外部驱动器上的Archlinux。我这样做是为了让我的Windows完好无损，因为我正慢慢离开它。要使用Archlinux，只需按F12键并选择Archlinux即可重新启动。当我需要做演示时，我只需重新启动到Windows。

我计划这样做，直到2018年6月中旬，我将彻底删除Windows作为我的主要操作系统，并把Archlinux。这是一个缓慢的举措，我想确保我得到所需的工具。它在向老板展示一个新想法时开始编写命令。

### 必需的工具和应用程序

在迁移到Linux时，以下是我使用的应用程序，它们的工作方式与Windows相同，甚至更好。

* 中文字体
* 搜狗输入法
* 办公室套装
* PDF呈现
* 微信桌面
* WhatsApp
* QQ桌面
* 磁盘管理
* 压缩文件


### 磁盘管理

从Windows环境迁移到Linux时，您可能会遇到的挑战之一就是偶尔检查磁盘。要做到这一点，您可以简单地从Linux安装Windows格式化磁盘。 Preety容易吗？咦？
不是真的。它们将作为只读进行装载。安装ntfs-3g软件包以删除只读锁

#### 安装

```控制台
sudo pacman -S ntfs-3g
```
安装完成后，您可以轻松安装NTFS格式化磁盘。

如果您对上述步骤有任何疑问，请写信您在下面评论部分的评论:-)