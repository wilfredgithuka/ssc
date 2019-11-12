+++
author = "Wilfred Githuka"
categories = ["linux"]
date = "2019-01-21"
description = "My Thoughts Sequence On How I Solved An Emacs-TeX Problem"
featured = ""
featuredalt = ""
featuredpath = ""
linktitle = ""
title = "Emacs+LaTeX+AuCTeX+CJKutf8 Fonts Problem"
type = "post"

+++
Today is a Monday and I have still not solved the Chinese input on Emacs issue. But I have decided to hold it
for a while since I have 2 pending reports to write. I plan to use emacs to write the English version then wps
to produce the Chinese version. But today mornning I realised that my latex setup is still not complete. There
are some errors during the compilation of AuCTEX to pdf. AuCTEX reports that: AUCTeX cannot find a working
TeX distribution. After scouring some documentaton I think the problem could be my zsh PATH variable which is
not correctly configured.

## Tex Live
Let me first install TeX live and see wether I can solve this problem. TeX live comes in 2 packages:

* teXLive-core (160MB)
* teXLive-most (600MB)

So I choose the core package since the reports are due soon.

sudo pacman -S texlive-core

After 15mins the installation is complete.

I have checked that the error seems to have gone, but I now have an issue. Last time I used a code to enable
TeX to render Chinese characters in the pdf file. This was possible by adding the following:

\usepackage{CJKutf8}

\begin{document}
\begin{CJK*}{UTF8}{gbsn

\end{CJK*

I cant seem to remember how I did this and I think this is contributing to the error.

Let me check-up on how to solve this.

This is a statement that I just got from a stackexchange website, but I forgot to not down the address. The
write has cleared the air on this mysterious CJKutf8 stuff. Read along...

CJKutf8 package is a part of CJK bundle, it is designed for documents in UTF-8 encoding only,
and it actually loads CJK package internally.The main aim of CJKutf8 package is,
to use utf8 option in inputenc package together with CJK package. That is to say, CJKutf8 patches
original CJK package to make it work well with inputenc. And it loads inputenc package with utf8 option internally.
Most users do not need to know the technical details. But you can use CJKutf8 to typeset French,
German and Chinese in one document easily. That's it.

After reading the above I decided to dig more in the Archwiki site and discovered some new stuff.
This article about [TeX and CJK](https://wiki.archlinux.org/index.php/TeX_Live_and_CJK) says that
I need to have texlive-langcjk installed. But after searching for it its not available, or even exist.
So I have gone back to the TeX page of the wiki and discovered that there is a special package forgot
to install.

* texlive-lang group contains packages providing character sets and features for non-English languages.
* texlive-langextra provides language support for African, Arabic, Armenian, Croatian, Hebrew, Indic,
Mongolian, Tibetan and Vietnamese.

I will install the texlive-lang group first then see the outcome. But its 250MB large.

This installation took long so I went for lunch, after coming back and running the pdf production
again, it was successful.

What a process.

So now I have it working, I can work on my reports. The only problem remaining is the Chinese input.
I will figure out that later.






## References and Links
* [TeX Live on Archwiki](https://wiki.archlinux.org/index.php/TeX_Live#Installation)
