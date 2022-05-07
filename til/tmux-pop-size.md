---
content: ''
cover: ''
date: 2022-01-05
datetime: 2022-01-05 00:00:00+00:00
description: tmux popups can be sized how you like based on the % width of the tmux
  popups can be sized how you like based on the % width of the
long_description: tmux popups can be sized how you like based on the % width of the
  tmux popups can be sized how you like based on the % width of the
now: 2022-05-07 21:32:25.891409
path: pages/til/tmux-pop-size.md
slug: til/tmux-pop-size
status: published
super_description: tmux popups can be sized how you like based on the % width of the
  tmux popups can be sized how you like based on the % width of the
tags:
- tmux
- linux
- bash
templateKey: til
title: Tmux Pop size
today: 2022-05-07
year: 2022
---

tmux popups can be sized how you like based on the % width of the
terminal on creation by using the flags (h, w, x, y) for height, width,
and position.

``` bash
# normal popup
tmux popup figlet "Hello"
# fullscreen popup
tmux popup -h 100% -w 100% figlet "Hello"
# 75% centered popup
tmux popup -h 100% -w 75% figlet "Hello"
# 75% popup on left side
tmux popup -h 100% -w 75% -x 0% figlet "Hello"
```

![example video running these commands](https://images.waylonwalker.com/tmux-popup-position.gif)