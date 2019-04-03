---
title: "Adjusting Screen Brightness in Linux"
date: 2019-04-03T08:43:34Z
draft: false
---

Brightness is a very important factor when using any device in this mordern age. Many devices produce
a large amount of light which is not good to for our eyes. To reduce the amount of light from your
device's screen, enable/use a dark theme.

In Linux, screen brightess is rather complex and I hope this brief article will help you understand.

The brightness of the screen backlight is adjusted by setting the power level of the backlight LEDs or cathodes.
The power level can often be controlled using the ACPI kernel module for video.

An interface to this module is provided via a sysfs directory at /sys/class/backlight/.

## Adjusting The Brightness

For this post I will be using a DELL laptop. First of all most commands require root access, so log-in as root.

List the backlight graphics model:

```console
ls sys/class/backlight/intel_backlight
```
The maximum brightness can be found by reading from max_brightness, which is often 15.

```console
cat sys/class/backlight/intel_backlight/max_brightness
```

To set a specific brightness, add it to the brightness variable.

```console
echo > 100 sys/class/backlight/intel_backlight/brightness
```
You can set whichever value you want depending on the brightness you require.

### References

* [Archlinux Wiki] (https://wiki.archlinux.org/index.php/backlight#Overview)




