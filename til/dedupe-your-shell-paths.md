---
content: ''
cover: ''
date: 2022-03-04
datetime: 2022-03-04 00:00:00+00:00
description: 'If you have ever ran  If you have ever ran '
long_description: 'If you have ever ran  If you have ever ran '
now: 2022-05-07 21:32:25.891987
path: pages/til/dedupe-your-shell-paths.md
slug: til/dedupe-your-shell-paths
status: published
super_description: 'If you have ever ran  If you have ever ran '
tags:
- linux
- cli
templateKey: til
title: Dedupe your shell paths
today: 2022-05-07
year: 2022
---

If you have ever ran `which <command>` and see duplicate entries it's likely
that you have duplicate entries in your $PATH.  You can clean this up with a
one liner at the end of your bashrc or zshrc.

``` bash
eval "typeset -U path"
```