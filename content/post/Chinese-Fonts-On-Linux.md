---
title: "Chinese Fonts on a Linux System"
date: 2019-05-05T09:53:35Z
categories: ["linux"]
tags: ["fonts", "wqy-microhei", "wqy-zenhei"]
draft: false
---

If your computer can't render the title of this post, you need to install the correct Chinese. The process is preety straight-forward except
for some small things.

### Fonts
Chinese fonts are quite unique and in Linux, you need to install some specific fonts to make the rendering more clear.
The following fonts will make Chinese Chracters rendering better on your linux machine.

#### Adobe Source Sans Sans
The Source Han Sans is a set of OpenType/CFF Pan-CJK fonts.Its an open source project that provides all of the source code files.
You can check out the [Github](https://github.com/adobe-fonts/source-han-sans) repo for the project.

Its interesting to note that this repo is about 1.6GB. This fonts were last updated in 2017 so they are good.

##### Installation

```console
sudo pacman -S adobe-source-han-sans-cn-fonts adobe-source-han-sans-tw-fonts adobe-source-han-serif-cn-fonts adobe-source-han-serif-tw-fonts
```

In the above commands, cn and tw means Chinese and Taiwan. Simplified and Traditional Chinese characters.
The first pair are sans while the second pair are serif fonts. The whole package is about 145MB.

#### The Wen Quan Yi Project Fonts Set

A Chinese friend recomended to me this set. Its a project that seeks to create high quality open-source bitmap and outline fonts for all Chinese Japan and Korean fonts.Since its open source, most dirstros have adopted this set. The name when translated to english means, the spring of letters. More about the project can be found on the [website](https://www.wenq.org). Wikipedia has a great [article](https://en.wikipedia.org/wiki/WenQuanYi) on the projet too.

##### Installation

On Archlinux, you can get 3 types of wqy fonts:- wqy-microhei, wqy-zenhei, wqy-bitmapfont

# 中文版

### 字体
中文字体非常独特，在Linux中，您需要安装一些特定的字体以使渲染更加清晰。以下字体将使您的Linux机器上的中文字符更好地呈现。

#### Adob​​e Source Sans Sans
Source Han Sans是一套OpenType / CFF Pan-CJK字体。它是一个提供所有源代码文件的开源项目。你可以查看该项目的[Github]（https://github.com/adobe-fonts/source-han-sans）回购。有趣的是，这个回购约为1.6GB。这些字体最后在207年更新，因此它们很好。

##### 安装

```控制台
sudo pacman -S adobe-source-han-sans-cn-fonts
sudo pacman -S adobe-source-han-sans-tw-fonts
sudo pacman -S adobe-source-han-serif-cn-fonts
sudo pacman -S adone-source-han-serif-tw-fonts
```
在上面的命令中，cn和tw表示中国和台湾。简体和繁体中文字符。第一对是无花果，而第二对是衬线字体。整个软件包大约是141MB。

#### 文泉易项目字体集

一位中国朋友向我推荐了这一套。它是一个旨在为所有中国日本和韩国字体创建高质量开源位图和轮廓字体的项目。自开源以来，大多数展示机构都采用了这一套。翻译成英文时的名字意味着信件的春天。有关该项目的更多信息可以在[网站]（https://www.wenq.org）上找到。 Wikipedia上也有一篇很棒的文章（https://en.wikipedia.org/wiki/WenQuanYi）。

##### 安装

在Archlinux上，你可以得到3种类型的wqy字体： - wqy-microhei，wqy-zenhei，wqy-bitmapfont

