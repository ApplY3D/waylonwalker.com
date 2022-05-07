---
content: ''
cover: ''
date: 2022-01-06
datetime: 2022-01-06 00:00:00+00:00
description: I I It turns out they are tabs, and you can get rid of the little leading
  It turns out they are tabs, and you can get rid of the little leading
long_description: I I It turns out they are tabs, and you can get rid of the little
  leading It turns out they are tabs, and you can get rid of the little leading
now: 2022-05-07 21:32:25.892178
path: pages/til/remove-vim-tab-characters.md
slug: til/remove-vim-tab-characters
status: published
super_description: I I It turns out they are tabs, and you can get rid of the little
  leading It turns out they are tabs, and you can get rid of the little leading
tags:
- vim
- linux
templateKey: til
title: Remove Vim Tab Characters
today: 2022-05-07
year: 2022
---

I've been stuck many times looking at a vim buffer with little question
marks at the beginning of each line and trying to get rid of them.  for
so long I didn't know what they were so trying to get rid of them was
impossible.

![example of what the tab character renders as in my editor](https://images.waylonwalker.com/vim-tab-characters.png)

It turns out they are tabs, and you can get rid of the little leading
question marks with this substitution command.

``` vim
:%s/\t/    /g
```