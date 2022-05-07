---
content: ''
cover: ''
date: 2021-07-20
datetime: 2021-07-20 00:00:00+00:00
description: https://youtu.be/hpFYE2LU7xc https://youtu.be/hpFYE2LU7xc Resizing panes
  in tmux can be quite difficult in default tmux, I Resizing panes in tmux can be
  quite d
long_description: https://youtu.be/hpFYE2LU7xc https://youtu.be/hpFYE2LU7xc Resizing
  panes in tmux can be quite difficult in default tmux, I Resizing panes in tmux can
  be quite difficult in default tmux, I Most often when I need to resize panes I just
  grab the edge of
now: 2022-05-07 21:32:25.894387
path: pages/blog/tmux-resize-panes.md
slug: tmux-resize-panes
status: published
super_description: https://youtu.be/hpFYE2LU7xc https://youtu.be/hpFYE2LU7xc Resizing
  panes in tmux can be quite difficult in default tmux, I Resizing panes in tmux can
  be quite difficult in default tmux, I Most often when I need to resize panes I just
  grab the edge of the pane with my Most often when I need to resize panes I just
  grab the edge of the pane with my https://waylonwalker.com/tmux-nav-2021/ https://waylonwalker.com/tmux-nav-2021/
  for more information on how I navigate tmux, check out this full post fo
tags:
- cli
- linux
- tmux
templateKey: blog-post
title: tmux resize-panes
today: 2022-05-07
year: 2021
---

https://youtu.be/hpFYE2LU7xc

Resizing panes in tmux can be quite difficult in default tmux, I
use a set of keybingings to help resize panes in the rare occasions
that I do need just a bit more space.  I set the keybinding to the same as my
split navigation bindings but shifted. They are very vim like (h,j,k,l).

``` bash
# resize panes
#―――――――――――――――――――――――――――――
bind -n M-H resize-pane -L 2
bind -n M-L resize-pane -R 2
bind -n M-K resize-pane -U 2
bind -n M-J resize-pane -D 2
```

Most often when I need to resize panes I just grab the edge of the pane with my
mouse.  Yes the mouse, its not that often that I actually need to change the
size of a pane.

``` bash
# Enable mouse control (clickable windows, panes, resizable panes)
set -g mouse on
```


  <div class="onelinelink-wrapper">
      <a class="onelinelink" href="https://waylonwalker.com/tmux-nav-2021/">
          <img style="float: right;" align='right' src="https://images.waylonwalker.com/tmux-nav-2021-og_250x140.png" alt="article cover for 
 How I navigate tmux in 2021
"/>
          <p><strong>
 How I navigate tmux in 2021
</strong></p>
      </a>
  </div>


> for more information on how I navigate tmux, check out this full post