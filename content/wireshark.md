---
title: Wireshark
menu: main
---
[Wireshark](https://www.wireshark.org) is the world's foremost network protocol analyzer. 
It lets you see what's happening on your network at a microscopic level. 
It is the de facto (and often de jure) standard across many industries and educational institutions.

Enable non-root users to use network interfaces:
```sh
$ sudo dpkg-reconfigure wireshark-common
$ sudo adduser $USER wireshark
```
