---
title: Solve Wifi Drops on Thinkpad T440
date: 2020-12-28 15:06:46
tags: 
  - Thinkpad
  - Wifi
categories:
  - Tips
---

Sometime my wifi speed drops on my thinkpad T440, so here's some configuration that might help.

## 1. Disable NetworkManager Powersave

* Edit `/etc/NetworkManager/conf.d/default-wifi-powersave-on.conf`
* Change `wifi.powersave = 3` to `wifi.powersave = 2`
* restart `NetworkManager` service

## 2. Disable 11n on iwlwifi

* Edit `/etc/modprobe.d/iwlwifi.conf`
* Add `options iwlwifi 11n_disable=1`
* Restart the configuration 
  ```
  $ sudo modprobe -r iwlmvm
  $ sudo modprobe -r iwlwifi
  $ sudo modprobe iwlwifi
  ```

source: https://gist.github.com/jcberthon/ea8cfe278998968ba7c5a95344bc8b55
