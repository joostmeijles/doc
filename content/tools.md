---
title: Tools
menu: main
---


- Set Java VM memory:
```
/etc/eclipse.ini
```
- Check mounts:
```
df -h
```
- Mapview:
```
mv2 [-r latest]
```
- Regression tests:
```
~/Projects/MPA_Regression/trunk/data/conversions/dev_telematics/
```
- `ssh win7vm06` Build on Windows
- `ssh msbld614` Build on Ubuntu 14.04
- To debug a dynamically loaded library with GDB (make sure that shared libraries contain debug symbols, this is e.g. not the case for MapAPI releases):
    `gdb> set environment LD_PRELOAD <librarytodebug.so>`
    `gdb> set environment LD_LIBRARY_PATH <library path>`
    `gdb> dir <source directory>` This seems to be optional
    Next set a breakpoint at the start of the program (such that the so gets loaded) and run GDB. At the breakpoint you should be able to load the source file from the so.
- GDB sometimes hangs upon start, to reset GDB: `rm -Rf ~/.ddd`
- Set breakpoint at catch in GDB: `catch catch`
- rsync -ave ssh from-machine:/dir/ /to/dir/
