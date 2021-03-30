---
title: Thinkfan Setup
date: 2021-03-28 20:52:10
tags:
  - Thinkpad
categories:
  - Tips 
---

# Thinkfan Setup

https://gist.github.com/Yatoom/1c80b8afe7fa47a938d3b667ce234559#gistcomment-3306472


# Manually set fan speed
```sh
echo enable |  sudo tee /proc/acpi/ibm/fan && echo level 4 | sudo tee /proc/acpi/ibm/fan
```
