---
title: Tools
menu: main
---

- Check mounts:
```bash
$ df -h
```

- Remote copy files using rsync
```bash
$ rsync -ave ssh from-machine:/from/dir/ /to/dir/
```

To set UTF-8 as default for Gnome terminal:
```bash
$ gconftool --set --type=string /apps/gnome-terminal/profiles/Default/encoding en_US.UTF-8
```
