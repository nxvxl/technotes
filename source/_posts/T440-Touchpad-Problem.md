---
title: T440 Touchpad Problem
date: 2020-08-04 11:11:05
tags:
  - Hardware
  - Thinkpad
categories:
  - Tips
---

- comment / remove `i2c_i801` from `/etc/modprobe.d/blacklist.conf`
- put `psmouse.sytnaptics_intertouch=0` into `GRUB_CMDLINE_LINUX` on `/etc/default/grub`
