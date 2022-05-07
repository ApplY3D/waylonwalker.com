---
canonical_url: https://waylonwalker.com/til/tmux-pop-size/
cover_image: https://images.waylonwalker.com/til/tmux-pop-size.png
description: tmux popups can be sized how you like based on the % width of the tmux
  popups can be sized how you like based on the % width of the
published: true
tags:
- tmux
- linux
- bash
title: Tmux Pop size
---

tmux popups can be sized how you like based on the % width of the terminal on creation by using the flags (h, w, x, y) for height, width, and position.

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