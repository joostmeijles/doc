---
title: Git
menu: main
---

[Git](https://git-scm.com) (/ɡɪt/) is a version control system that is used for software development
and other version control tasks. As a distributed revision control system it 
is aimed at speed, data integrity, and support for distributed, non-linear workflows.

To fixup and squash commits in a branch read [this](http://fle.github.io/git-tip-keep-your-branch-clean-with-fixup-and-autosquash.html).

A list of useful Git commands can be found [here](http://orga.cat/posts/most-useful-git-commands).

To list remote sites:
```
$ git remote -v
```

To set remote url for a site, e.g. for switching from using HTTPS to SSH:
```
$ git remote set-url origin git@github.com:<username>/<repository>.git
``` 
