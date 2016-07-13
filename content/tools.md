---
title: Tools
menu: main
---


- List projects:
```
cmsutil list
```
- Generate Eclipse xml includes:
```
/data/users/public/reinco.hof/cms2ecl distr
```
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
- Regression test results:
```
/data/users/attreg/regconv/dev_telematics
```
- `/data/id/release/` Releases; .convert script will search here for matching bundle/product
- `export CVTOOL_DEBUG_COMMAND="valgrind --leak-check=full --show-reachable=yes --track-origins=yes {EXE} {ARGS} 2> {EXE}.valgrind` Wrap command around every program started by Dakota (CV) tool (David Ingamells)
- `export CVTOOL_DEBUG_PROCESSES="SFMBuildTraces"` Specify which process to debug, needs to be set in combination with Dakota Debug wrapper command
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
- Determine changes between releases:
```
/data/id/release/VVVTools/TestTools_latest/x86_64_Ubuntu_14.04/MapTestRegressionTest/scripts/gettaskchanges.sh NDS/nds_toolkit_20160326 NDS/nds_toolkit_20160329 --browser
```
