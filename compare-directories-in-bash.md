---
content: ''
cover: ''
date: 2020-12-11
datetime: 2020-12-11 00:00:00+00:00
description: Today I needed to check for articles that used the same slug from two
  directories, bash made it super simple. Today I needed to check for articles that
  used the
long_description: Today I needed to check for articles that used the same slug from
  two directories, bash made it super simple. Today I needed to check for articles
  that used the same slug from two directories, bash made it super simple.
now: 2022-05-07 21:32:25.892924
path: pages/blog/compare-directories-in-bash.md
slug: compare-directories-in-bash
status: draft
super_description: Today I needed to check for articles that used the same slug from
  two directories, bash made it super simple. Today I needed to check for articles
  that used the same slug from two directories, bash made it super simple.
tags:
- bash
- tip
templateKey: hot-tip
title: Compare Directories In Bash
today: 2022-05-07
year: 2020
---

Today I needed to check for articles that used the same slug from two directories, bash made it super simple.

``` bash
diff -rq src/pages/blog src/pages/notes
```