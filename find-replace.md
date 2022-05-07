---
content: ''
cover: ''
date: 2020-11-12
datetime: 2020-11-12 00:00:00+00:00
description: notes about find and replace techniques
long_description: ''
now: 2022-05-07 21:32:25.892436
path: pages/notes/find-replace.md
slug: find-replace
status: published
super_description: ''
tags:
- linux
- bash
templateKey: blog-post
title: Find and Replace in the Terminal.
today: 2022-05-07
year: 2020
---

## grepr

```bash
grepr() {grep -iRl "$1" | xargs sed -i "s/$1/$2/g"}

```bash
grepr() {grep -iRl "$1" | xargs sed -i "s/$1/$2/g"}
```

## grepd

``` python
grepd() {grep -iRl "$1" | xargs sed -i "/^$1/d"}
```

## CocSearch


``` bash
:CocSearch status: 'false' -g *.md
```