+++
author = "Wilfred Githuka 楚大洋"
categories = ["latex"]
date = "2018-11-12"
description = "How To Make A Cover Page + Other Small Modifications"
featured = ""
featuredalt = ""
featuredpath = "date"
linktitle = ""
title = "Cover Page(ing) For Your Latex Document"
type = "post"

+++
![image1](/img/sun.JPG)

For a while now I have been pondering on how I can add a cover page to my weekly report to make it look more presentable. It will also give me more room to write content that would other have to be dropped onto the next page. This weekend I dug up on my Latex documentation to find out how I can add a cover page. It was however no straight forward as I thought, but I found workarounds.

### Cover Page Setup
This was completely done on its own document which I would merge later with the main report after am done. I used a template from the awesome guys over at [Wiki-Title Creation](https://www.latextemplates.com) who were the original authors of the document.

Even though this templete came in clean, I had to make some changes since the introduction of a Chinese font didn't go down well. This is firstly because of the emphasis text command

\textsc{淹死的都是会游泳的}

When you run the above command it will kill the first character 淹 while show the rest sentence. The killed character will be replaced by unreadable text. To get aroud this add some more changed to the text like increasing the size of text.

\textsc\large{淹死的都是会游泳的}

This will solve the problem. Note that there are more commands under emphasis text that are worth learning about. 

* \emp{}: italics
* \textit{}: italics
* \textbf{}: bold
* \texttt{}: typewriter
* \textsf{}: sans-serif
* \textsc{}: CAPITAL
 
 This guy at [Texblog](https://textblog.org/about/) explains better.
 
#### Extra Page On Cover Page Issue

After doing some minor modifications, I ran it and the resulting pdf had an extra page being created ahead of the title page. This was caused as I understand by the addition of the Chinese character enabler:

\usepackage{CJKutf8}
\begin{document}
\begin{CJK*}{UTF8}{gbsn}
.
.
.

No matter where I placed the command, the extra page was still being created. I resulted to removing the page later after the pdf was created. Not a good workaround, am sure there is a way to solve this.

### Final Merging
Since I had two documents, I needed to merge them into one. I think TeX can do this but for now I used pdfunite to do this. The command is:

```terminal
pdfunite cover.pdf report.pdf out.pdf
```
