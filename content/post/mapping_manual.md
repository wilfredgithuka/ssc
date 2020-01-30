---
title: "Mapping Project 说明书"
date: 2020-01-30T08:44:30+03:00
draft: false
---

## 安装 Anaonda编程环境

Anaconda 编程环境是个很好的编程工具包。你先打开[这个网站](https://www.anaconda.com/distribution/#download-section)，

然后下载Anaconda的Bash Script. 注意选择根据你现在使用的主系统。

首先执行(换允许) 
```
chmod +x script-name-here.sh
```
然后可以直接执行
```
./script-name-here.sh
```
在 ~/.zshrc 加一下的内容：

```
unset __conda_setup
# <<< conda initialize <<<
```

然后执行
```
/home/wilfred/miniconda3/bin/conda init zsh
```
打开新的Terminal窗户，看看有没有Conda成功

## 安装配合软件

创建一个新的工作环境
```
conda create -n mapping
```
然后启用
```
conda activate mapping
```
安装工具
```
conda install mapping
```
到时候Anaconda会自动开始安装相关的工具软件。轻笑等。。。
你可以随时更新Anacoda:
```
conda update -n base -c defaults conda
```
成功，您的Anaconda环境现在可以开始使用。
