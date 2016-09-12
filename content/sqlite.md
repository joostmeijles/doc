---
title: Sqlite
menu: main
---

[SQLite|https://www.sqlite.org] is a software library that implements a self-contained, serverless, zero-configuration, transactional SQL database engine.
SQLite is the most widely deployed database engine in the world. The source code for SQLite is in the public domain.

To show table schema:
```
sqlite> .schema table
```

To exit SQLite console:
```
sqlite> .exit
```

To switch table headers on:
```
sqlite> .header on
```

To attach another database:
```
sqlite> attach "<database>.sq3" as ref;
```
