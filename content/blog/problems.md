+++
author = "Wilfred Githuka"
categories = ["linux"]
date = "2019-01-24"
description = "Some Of The Issues Am Yet To Fix On My Linux Machine In Regards To Chinese"
featured = ""
featuredalt = ""
featuredpath = ""
linktitle = ""
title = "Minor Issues Unfixed So Far 我的电脑上的小问题"
type = "post"

+++
The following are some of the issues which remain unsolved so far in my ArchLinux i3 Chinese
machine. Some are language specific, some are just system based configuration.

## No Chinese Input Support in Spacemacs
This is by far the biggest issue am yet to solve. Last year I remeber solving this issue 
but because I did not document my process, after re-installing Archlinux I have to do it again.

Here is where the importance of documenting one's progress.

I have however made some attempt and you can read my [thought process here]( https://chinese.githuka.com/blog/emacs_chinese_input/)

There is still no success. But am working on it.

## [SOLVED]Windows Size Out Of Screen
The dialog box is always out of resolution and sometimes I cannot see the file name especially when saving a document from
the internet. I suppose this is a Chromium issue, but its very frustrating.

### Solution

The maximum and minimum dimensions of floating windows can be specified. If either dimension of floating_maximum_size is specified as -1, that dimension will be unconstrained with respect to its maximum value. If either dimension of floating_maximum_size is undefined, or specified as 0, i3 will use a default value to constrain the maximum size. floating_minimum_size is treated in a manner analogous to floating_maximum_size.

A more simpler solution is to just hold the `mod+right-click` when the window pops up the drag to resize to the appropriate size.

Problem Solved.
## No Chinese Input Support in Terminal - Zsh
I still dont have Chinese charcter support in oh-my-zsh. I think its a fonts problem since I can input Chinese characters
but they show up as boxes.

## Copy Paste Issues in Zsh
How does one copy-paste in oh-my-zsh?

## Printer Suport is Having Issues. Blank Page Printout
This I tend to think its a driver issue for the printer. When I send a file to the printer, I get a blank output while
the printer goes into a printing frenzy.

## WeChat Support/alternative in ArchLinux
The Linux [Wechat app]( https://github.com/geeeeeeeeek/electronic-wechat) that I used to have is no longer maintained. 项目不再维护.
There is a tutorial here on [Linux Babe]( https://www.linuxbabe.com/desktop-linux/install-wechat-linux) which I will try out later.

## PDF Preview support in Ranger
Ranger is an awesome file manager. I know that It has an awesome PDF preview. Oh-my-zsh I think it should have a PFD preview which
should come in handy when scanning many documents.

## [Solved] Android USB Tethering Support
This issue I have since resolved it well and you can read the solution [here]( https://chinese.githuka.com/blog/filemanager/)

## [Projector Connection Issue]
Projector connection is not so straightforward as it is on Windows. However after reading some online documentation, am almost
there to attain successful connection to a projector. This might come in handy if am told to give a presentation in the future.
There is an application called [arandr](https://www.archlinux.org/packages/?name=arandr) that should simply the process according to the 
documentation for [xrandr](https://wiki.archlinux.org/index.php/Xrandr)
