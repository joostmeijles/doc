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

Start program with GDB attached:
```
$ gdb -ex=r --args <program>
```

A cheat sheet with GDB commands can be found [here](https://people.eecs.berkeley.edu/~mavam/teaching/cs161-sp11/gdb-refcard.pdf).

To debug a dynamically loaded library with GDB (make sure that shared libraries contain debug symbols, this is e.g. not the case for MapAPI releases):
```
gdb> set environment LD_PRELOAD <librarytodebug.so>
gdb> set environment LD_LIBRARY_PATH <library path>
gdb> dir <source directory>
```
Next set a breakpoint at the start of the program (such that the so gets loaded) and run GDB. At the breakpoint you should be able to load the source file from the shared object.

GDB sometimes hangs upon start, to reset GDB:
```
$ rm -Rf ~/.ddd
```

To set a breakpoint at catch in GDB:
```
gdb> catch catch
```
