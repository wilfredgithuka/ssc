---
title: "New WPS 11.1.0.8392-2 unstable on Archlinux"
date: 2019-05-20T08:19:02Z
draft: false
---

I seem to be the only one facing unstable issues on the new WPS Office
suite on my Archlinux machine running i3wm.

The new WPS suite really looks appealing. The UI team really outdid
themselves this time round. No sharp edges and smooth opening of menus.

Even after upgrading my machine, I still exprerienced the following issues:

* WPS Window dissapering after moving from one workplace to another.
* Freezing more often
* No support for Chinese input with fcitx

For this reason I had to downgrade back to version 10.1.0.6758.

## How To Downgrade a Package?

This is preety simple.

```
yay -U wps-office_10.1.0.6758_x86_64.tar.xz
```
I will use this one until I find a work-around the problem.

Have a goodday, won't you?
