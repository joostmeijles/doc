---
title: Debian
menu: main
---
[Debian](http://www.debian.org) is a free operating system (OS) for your computer.
Debian package management is for example used for [Ubuntu](http://www.ubuntu.com) packages.

To show package contents:
```bash
$ dpkg -c <package>
```

To show package meta info:
```bash
$ dpkg-deb -I <package>
```

To force install using apt-get:
```bash
$ sudo apt-get -o Dpkg::Options::="--force-overwrite" install <package>
```

How to setup the micro firewall: [ufw](https://www.digitalocean.com/community/tutorials/how-to-setup-a-firewall-with-ufw-on-an-ubuntu-and-debian-cloud-server)
```bash
$ sudo ufw
```

Show latest ran cron jobs:
```bash
$ sudo grep -i cron /var/log/syslog | tail -2
```

Enabling core dumps [explained here](http://www.akadia.com/services/ora_enable_core.html).

To change SUDO behavior:
```bash
$ visudo
visudo> username ALL=(ALL) NOPASSWD:ALL
```

To list open file descriptors per pid:
```bash
$ lsof -p <pid>
```

Number of open files on Linux: http://www.cyberciti.biz/faq/linux-increase-the-maximum-number-of-open-files/

To set ulimit system wide:
```bash
$ sudo vim /etc/security/limits.conf
```

An easy memory usage overview can be obtained using [coremem](https://github.com/crquan/coremem).

The difference between *ps* vs *top* cpu usage  [explained](http://unix.stackexchange.com/questions/58539/top-and-ps-not-showing-the-same-cpu-result).

To trace function calls, [etrace](http://ndevilla.free.fr/etrace/) can be used.

Filesytem over SSH: [SSHFS](https://www.digitalocean.com/community/tutorials/how-to-use-sshfs-to-mount-remote-file-systems-over-ssh).
