---
content: ''
cover: ''
date: 2022-02-23
datetime: 2022-02-23 00:00:00+00:00
description: Git has a built in way to rebase all the way back to the beginning of
  Git has a built in way to rebase all the way back to the beginning of
long_description: Git has a built in way to rebase all the way back to the beginning
  of Git has a built in way to rebase all the way back to the beginning of
now: 2022-05-07 21:32:25.891559
path: pages/til/git-rebase-root.md
slug: til/git-rebase-root
status: published
super_description: Git has a built in way to rebase all the way back to the beginning
  of Git has a built in way to rebase all the way back to the beginning of
tags:
- git
- cli
templateKey: til
title: Git rebase to the beginning of time
today: 2022-05-07
year: 2022
---

Git has a built in way to rebase all the way back to the beginning of
time.  There is no need to scroll through the log to find the first
hash, or find the total number of commits. Just use `--root`.

``` bash
git rebase --root
```