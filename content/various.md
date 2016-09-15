---
title: Various
menu: main
---

- Embed text in object file: http://www.linuxjournal.com/content/embedding-file-executable-aka-hello-world-version-5967
- `grep -A1 [text] [file]`
- `du -hs * | sort -h`
- Overlapping static instances: http://stackoverflow.com/questions/6714046/c-linux-double-destruction-of-static-variable-linking-symbols-overlap
- Controlling symbol visibility: http://www.ibm.com/developerworks/aix/library/au-aix-symbol-visibility/ and http://www.akkadia.org/drepper/dsohowto.pdfdud
- Enabling core dumps: http://www.akadia.com/services/ora_enable_core.html
- Show latest cron jobs
```
sudo grep -i cron /var/log/syslog|tail -2
```
-
```
sudo apt-get -o Dpkg::Options::="--force-overwrite" install <package name>
```
- Firewall setup: https://www.digitalocean.com/community/tutorials/how-to-setup-a-firewall-with-ufw-on-an-ubuntu-and-debian-cloud-server
```
sudo ufw
```  
- Activate newly created users group:
```
newgrp docker
```
- Easy memory usage overview: https://github.com/crquan/coremem
- C10K discussion: http://www.kegel.com/c10k.html#nb.edge
- List open file descriptors per pid:
```
lsof -p <pid>
```
- Number of open files on Linux: http://www.cyberciti.biz/faq/linux-increase-the-maximum-number-of-open-files/
- To allow su to set ulimit, edit and uncomment pam_limits.so in: /etc/pam.d/su
- Set ulimits system wide, note that root permissions need to be set explicitly: /etc/security/limits.conf
- Lookup open sockets:
```
while [ 1 ]; do sudo lsof -p `pidof <proc name>` | grep ESTABLISHED | wc; sysctl fs.file-nr; sleep 1; done
```
- TCP backlog in Linux: http://veithen.github.io/2014/01/01/how-tcp-backlog-works-in-linux.html
- TCP TIME_WAIT: http://vincent.bernat.im/en/blog/2014-tcp-time-wait-state-linux.html
- TCP_NODELAY: http://www.ibase.ru/devinfo/tcp_nodelay.txt
- C10K problem: http://www.kegel.com/c10k.html
- Some benchmark rules: https://www.mnot.net/blog/2011/05/18/http_benchmark_rules
- ps cpu% vs top cpu%: http://unix.stackexchange.com/questions/58539/top-and-ps-not-showing-the-same-cpu-result
- Trace function calls: http://ndevilla.free.fr/etrace/
- Set UTF-8 as default for Gnome terminal:
```
gconftool --set --type=string /apps/gnome-terminal/profiles/Default/encoding en_US.UTF-8
```
- Socket reuse explained: http://stackoverflow.com/questions/14388706/socket-options-so-reuseaddr-and-so-reuseport-how-do-they-differ-do-they-mean-t
- HTTP workgroup page: http://httpwg.org/

- Change SUDO behavior:
```
> visudo
```
Add to last line:
```joost.meijles ALL=(ALL) NOPASSWD:ALL```

- SSHFS: https://www.digitalocean.com/community/tutorials/how-to-use-sshfs-to-mount-remote-file-systems-over-ssh


CCache with Memcached: https://gist.github.com/itensionanders/2bd0056027f8308d4cd8

Linux select vs. poll vs. epoll: http://www.ulduzsoft.com/2014/01/select-poll-epoll-practical-difference-for-system-architects/
POLLOUT explained: http://stackoverflow.com/questions/12170037/when-to-use-pollout
