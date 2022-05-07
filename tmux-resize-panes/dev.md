---
canonical_url: https://waylonwalker.com/tmux-resize-panes/
cover_image: https://images.waylonwalker.com/tmux-resize-panes.png
description: https://youtu.be/hpFYE2LU7xc https://youtu.be/hpFYE2LU7xc Resizing panes
  in tmux can be quite difficult in default tmux, I Resizing panes in tmux can be
  quite d
published: true
tags:
- cli
- linux
- tmux
title: tmux resize-panes
---

https://youtu.be/hpFYE2LU7xc

Resizing panes in tmux can be quite difficult in default tmux, I use a set of keybingings to help resize panes in the rare occasions that I do need just a bit more space.  I set the keybinding to the same as my split navigation bindings but shifted. They are very vim like (h,j,k,l).

``` bash
# resize panes
#―――――――――――――――――――――――――――――
bind -n M-H resize-pane -L 2 bind -n M-L resize-pane -R 2 bind -n M-K resize-pane -U 2 bind -n M-J resize-pane -D 2
```

Most often when I need to resize panes I just grab the edge of the pane with my mouse.  Yes the mouse, its not that often that I actually need to change the size of a pane.

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