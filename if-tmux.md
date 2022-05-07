---
content: ''
cover: ''
date: 2021-01-09
datetime: 2021-01-09 00:00:00+00:00
description: I do much of my work from tmux, I love it so much that I want to setup
  some I do much of my work from tmux, I love it so much that I want to setup some
  Bash fun
long_description: I do much of my work from tmux, I love it so much that I want to
  setup some I do much of my work from tmux, I love it so much that I want to setup
  some Bash function to check if the shell is in a tmux session. Bash function to
  check if the shell is i
now: 2022-05-07 21:32:25.892819
path: pages/blog/if-tmux.md
slug: if-tmux
status: published
super_description: I do much of my work from tmux, I love it so much that I want to
  setup some I do much of my work from tmux, I love it so much that I want to setup
  some Bash function to check if the shell is in a tmux session. Bash function to
  check if the shell is in a tmux session. I often open up vim to do some quite edits,
  but before I know it I have several I often open up vim to do some quite edits,
  but before I know it I have several Using  Using  I am not quite sure if this is
  proper use of the  I am not
tags:
- bash
- tmux
templateKey: blog-post
title: If Tmux
today: 2022-05-07
year: 2021
---

I do much of my work from tmux, I love it so much that I want to setup some
functionality that puts me in tmux even if I didn't ask for it.


## Bash Function

Bash function to check if the shell is in a tmux session.

``` bash
in_tmux () {
  if [ -n "$TMUX" ]; then
    return 0
  else
    return 1
  fi
  }
```

## Using the bash function

I often open up vim to do some quite edits, but before I know it I have several
splits open and I need access to another shell utility, but I forgot to start
in tmux.  This function makes sure tht I start in tmux everytime.

Using `if_tmux` to ensure vim is opened in tmux.

``` bash
vim () { 
  in_tmux \
    && nvim \
    || bash -c "\
    tmux new-session -d;\
    tmux send-keys nvim Space +GFiles C-m;\
    tmux -2 attach-session -d;
    "
  }
```


I am not quite sure if this is proper use of the `&&` and `||`, let me know if
you have a better way to do one thing if `in_tmux` returns true and another if
it returns faslse.