---
title: Synology
menu: main
---

Asterisk is no longer supported on DSM 6. It can however be installed using [Optware](https://github.com/Optware/Optware-ng).

To maintain Asterisk while upgrading from DSM 5 to DSM 6:

1. Add the following community package: https://www.cphub.net

2. Go to the Package Manager and install Easy Bootstrap Installer: this will install optware on your Synology.

3. Backup the Asterisk configuration using the backup GUI, or at least copy sip.conf, extensions.conf, and user.conf

4. Uninstall Asterisk from the DSM 5

5. After all updates are done, you should be able to use ipkg from the command line. Use SSH to login, from your admin account, to your Synology.

6. Install Asterisk 13 and GUI:
```bash
$ sudo ipkg install asterisk13 asterisk-gui
```

7. Test if your Asterisk installation runs:
```bash
$ sudo asterisk -vvv
```

8. Copy the backup files (not all are compatible) sip.conf, extensions.conf, and user.conf to /opt/etc/asterisk.

9. Enable the web GUI by editing manager.conf and http.conf, see [here](http://doc.astlinux.org/userdoc:tt_asterisk-gui).

10. To automatically run Asterisk upon start add an Upstart script to e.g. /etc/init/asterisk.conf:

```bash
start on runlevel [2345]
stop on runlevel [06]

exec /opt/sbin/asterisk
```
