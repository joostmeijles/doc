---
title: SSL
menu: main
---
SSL (Secure Sockets Layer) is the standard security technology for establishing
an encrypted link between a web server and a browser. This link ensures that all
data passed between the web server and browsers remain private and integral.

To create a SSL bundle (each certificate indicates its own dependent certificate):
```bash
$ cat server.crt intermediate.crt root.crt > ssl-bundle.crt
```

To verify a SSL certificate setup (note that openssl requires to have the root certificate locally, otherwise you get error 19 (self signed ...)):
```bash
$ openssl s_client -connect test-mbimup.navinfo.com:443 -CAfile GlobalSign-Root-R1.crt
```

How to debug certificates can be read [here](http://www.cyberciti.biz/faq/test-ssl-certificates-diagnosis-ssl-certificate/).

How to setup SSL with Nginx can be found [here](https://support.comodo.com/index.php?/Default/Knowledgebase/Article/View/789/37/certificate-installation-nginx).
