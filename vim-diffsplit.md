---
content: ''
cover: ''
date: 2021-05-06
datetime: 2021-05-06 00:00:00+00:00
description: ''
long_description: ''
now: 2022-05-07 21:32:25.894014
path: pages/blog/vim-diffsplit.md
slug: vim-diffsplit
status: draft
super_description: ''
tags:
- linux
- vim
templateKey: blog-post
title: How to compare two files in vim
today: 2022-05-07
year: 2021
---

``` vim
:vert diffsplit filetwo.py
```

``` vim
:diffthis
```

``` vim
:diffoff
```

``` vim
:Gdiff main
```