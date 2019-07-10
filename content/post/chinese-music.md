---
title: 从Youtube下载中国音乐 Download Chinese Music From Youtube
date: 2018-08-01T22:41:36+03:00
lastmod: 2018-08-01T22:41:36+03:00
author: Wilfred Githuka 楚大洋
cover: /img/music.jpg
categories: ["music", "音乐"]
tags: ["ffmpeg", "youtube-dl"]
draft: false
---

怎么下载中国音乐 How to download some good quality Chinese songs or mixes from
youtube and learn some info about media formats while at it. Oh and by the way
welcome to August 2018 :-)
<!--more-->

So August is here, we are almost hitting one month since our Welding Training
started here at The Kisii National Polytechnic-Kisii County. Everybody is
on high spirits as we wade through the waters of Welding Technology.

Sometimes all you want is a dose of the latest Chinese music on your linux
box especially when you have spent the whole weekend trying to get the
[Chinese layer](https://github.com/syl20bnr/spacemacs/tree/master/layers/%2Bintl/chinese#description) 
on [Spacemacs](https://github.com/syl20bnr/spacemacs/blob/master/doc/BEGINNERS_TUTORIAL.org#5-open-spacemacs-and-choose-default-editing-style) to work.

What do you do?

Youtube has your back on this one. Just follow these steps:

### 工具Tools
* youtube-dl
* ffmpeg 

### Youtube
From Youtube get to the song which you love and get the address to the
video, copy that to the clipboard.

### Linux Terminal
Fire up your favorite terminal emulator then start youtube-dl like this
then feed it the address to the video. Just paste the like there.

```console
youtube-dl youtube-dl https://youtu.be/fBW36l7zuQQ
```
Hit enter to start the download. If its a big file, grab a cup of coffee.
The file that will be downloaded shall be a .webm format which comprises
of both video and audio. Next we need to extract the audio to .mp3 format.

### ffmpeg
Note where the file has been downloaded then start ffmpeg with the
following code to do the conversion.

```console
FILE="the-file-you-want-to-process.webm";
ffmpeg -i "${FILE}" -vn -ab 128k -ar 44100 -y "${FILE%.webm}.mp3";
```
Hit enter to start the conversion process. Change the value to the 
variable FILE to the name of your .webm file.

Enjoy a clean .mp3 audio

## References
* [Bytefreaks.net](https://bytefreaks.net/gnulinux/bash/ffmpeg-extract-audio-from-webm-to-mp3)