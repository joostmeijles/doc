---
title: Mongo DB
menu: main
---

[MongoDB](http://www.mongodb.org) (from humongous) is a free and open-source cross-platform document-oriented database.
Classified as a NoSQL database, MongoDB avoids the traditional table-based relational database
structure in favor of JSON-like documents with dynamic schemas (MongoDB calls the format BSON),
making the integration of data in certain types of applications easier and faster.

To copy a database:
```bash
mongo> db.copyDatabase("from-dbname","to-dbname","from.host.nl")
```
