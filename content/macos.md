---
title: MacOS
menu: main
---

To automatically mount network folders in MacOS:

Create a file containing the mount points, e.g. */etc/auto_nas*:
```bash
network-address -fstype=afp afp://user:password@address/directory
```
Use the newly created file in */etc/auto_master*:
```bash
/nas			auto_nas	-nosuid
```

Convert CDR (e.g. created using Disk Utility) to ISO:
```bash
$ hdiutil convert from.cdr -format UDTO -o to.iso
```
