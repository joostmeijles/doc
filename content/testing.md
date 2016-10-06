---
title: Testing
menu: main
---

- HTML response codes: http://httpstatus.es/

- Redirect to stdout and terminate after 1 second after connection is idle:
```bash
$ sudo socat -T1 TCP4-LISTEN:8080,reuseaddr STDOUT
```
- Show local network traffic on port 8080:
```bash
$ sudo tcpflow -Ci lo port 8080
```
- Show local network traffic matching PUT:
```bash
$ sudo ngrep -d lo '^PUT'
```
- TCP dump:
```bash
$ sudo tcpdump -i lo 'port 80' -w -
```
- Wireshark:
```bash
$ sudo apt-get install wireshark
$ sudo dpkg-reconfigure wireshark-common
$ sudo adduser $USER wireshark
```
- Wireshark ZeroMQ plugin: https://github.com/whitequark/zmtp-wireshark
- Test C++ code using GMock: http://yolyeng.blogspot.nl/2014/01/google-test-and-google-mock-using.html
