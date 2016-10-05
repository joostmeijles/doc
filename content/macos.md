---
title: MacOS
menu: main
---

To automatically mount network folders in MacOS:

Create a file containing the mount points, e.g. */etc/auto_nas*:
```
network-address -fstype=afp afp://user:password@address/directory
```
Use the newly created file in */etc/auto_master*:
```
/nas			auto_nas	-nosuid
```
