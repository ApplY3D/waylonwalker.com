---
content: ''
cover: ''
date: 2020-12-13
datetime: 2020-12-13 00:00:00+00:00
description: This is how I script a tmux layout This is how I script a tmux layout
long_description: This is how I script a tmux layout This is how I script a tmux layout
now: 2022-05-07 21:32:25.893514
path: pages/blog/scripting-tmux-layouts.md
slug: scripting-tmux-layouts
status: draft
super_description: This is how I script a tmux layout This is how I script a tmux
  layout
tags:
- bash
- tmux
templateKey: hot-tip
title: Scripting Tmux Layouts
today: 2022-05-07
year: 2020
---

This is how I script a tmux layout

``` bash
 bash -c "tmux new-session -t 'editor' -d;\
    tmux split-window -v 'zsh';
    tmux send-keys nvim Space /src/ Space +GFiles C-m; \
    tmux rotate-window; \
    tmux select-pane -U; \
    tmux -2 attach-session -d
    "
```