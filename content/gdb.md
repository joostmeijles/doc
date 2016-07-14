---
title: GDB
menu: main
---
The [GNU Debugger](https://www.gnu.org/software/gdb/), usually called just GDB and named gdb as an executable file, 
is the standard debugger for the GNU operating system.

To not let GDB handle signals:
```
gdb> handle SIGPIPE nostop noprint pass
```
