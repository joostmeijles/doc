---
title: Testing
menu: main
---

- Run regression test:
```
./start_regression -bundle dev_telematics -ref dev_telematics_20150529 -test dev_telematics_latest` Run regression test locally
```
- SFM definition of done: http://dokuwiki.mapscape.nl/doku.php?id=dev:sfm_telematics_dod
- HTML response codes: http://httpstatus.es/
- Redirect to stdout and terminate after 1 second after connection is idle:
```
sudo socat -T1 TCP4-LISTEN:8080,reuseaddr STDOUT
```
- Show local network traffic on port 8080:
```
sudo tcpflow -Ci lo port 8080
```
- Show local network traffic matching PUT:
```
sudo ngrep -d lo '^PUT'
```
- TCP dump:
```
sudo tcpdump -i lo 'port 80' -w -
```
- Wireshark:
```
sudo apt-get install wireshark
sudo dpkg-reconfigure wireshark-common
sudo adduser $USER wireshark
```
- Wireshark ZeroMQ: https://github.com/whitequark/zmtp-wireshark
- GMock: http://yolyeng.blogspot.nl/2014/01/google-test-and-google-mock-using.html
