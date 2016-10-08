---
title: Python
menu: main
---
[Python](https://www.python.org) is a programming language that lets you work quickly
and integrate systems more effectively.

The [PEP 8](https://www.python.org/dev/peps/pep-0008/) style guide for writing Python.

The difference between __str__ and __repr__ [explained](http://brennerm.github.io/posts/python-str-vs-repr.html).

Small script to recursively grep in files:
```python
import fnmatch
import os

filePattern  = '*.txt'
lineContains = 'paard'

def recursive_glob(rootdir='.', pattern='*'):
    return [os.path.join(looproot, filename)
            for looproot, _, filenames in os.walk(rootdir)
            for filename in filenames
            if fnmatch.fnmatch(filename, pattern)]


linesPerFile = []

for filename in recursive_glob(pattern=filePattern):
    lines = [line.strip() for line in open(filename) if lineContains in line]

    for line in lines:
        linesPerFile.append((line, filename))

linesPerFile.sort(key=lambda tuple: tuple[0])

for (line, file) in linesPerFile:
    print(line + ' -> ' + file)
```
