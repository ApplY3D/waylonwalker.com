---
canonical_url: https://waylonwalker.com/scripting-tmux-layouts/
cover_image: https://images.waylonwalker.com/scripting-tmux-layouts.png
description: This is how I script a tmux layout This is how I script a tmux layout
published: true
tags:
- bash
- tmux
title: Scripting Tmux Layouts
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