---
title: Sockets
menu: main
---

To lookup open sockets:
```bash
$ while [ 1 ]; do sudo lsof -p `pidof <proc name>` | grep ESTABLISHED | wc; sysctl fs.file-nr; sleep 1; done
```

How the Linux TCP backlog works is explained [here](http://veithen.github.io/2014/01/01/how-tcp-backlog-works-in-linux.html).

TCP states:

- [TCP TIME_WAIT](http://vincent.bernat.im/en/blog/2014-tcp-time-wait-state-linux.html)
- [TCP_NODELAY](http://www.ibase.ru/devinfo/tcp_nodelay.txt)

The [C10K problem](http://www.kegel.com/c10k.html).

Linux select vs. poll vs. epoll
[explained](http://www.ulduzsoft.com/2014/01/select-poll-epoll-practical-difference-for-system-architects/).

The POLLOUT event [explained](http://stackoverflow.com/questions/12170037/when-to-use-pollout).

Socket reuse [explained]( http://stackoverflow.com/questions/14388706/socket-options-so-reuseaddr-and-so-reuseport-how-do-they-differ-do-they-mean-t).
