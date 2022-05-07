---
canonical_url: https://waylonwalker.com/tmux-splitting-panes/
cover_image: https://images.waylonwalker.com/tmux-splitting-panes.png
description: https://youtu.be/kzgyiHap1nQ https://youtu.be/kzgyiHap1nQ splitting panes
  is a core feature of tmux.  It allows us to split the terminal splitting panes is
  a co
published: true
tags:
- cli
- linux
- tmux
title: tmux splitting panes
---

https://youtu.be/kzgyiHap1nQ

splitting panes is a core feature of tmux.  It allows us to split the terminal vertically or horizontally into new panes.

``` bash
bind -n M-s split-window -c '#{pane_current_path}' bind -n M-v split-window -h -c '#{pane_current_path}' bind -n M-X kill-pane
```

> 🗒️ note that  '#{pane_current_path}'will keep the split in the same directory
> as it's parent, without this it will default to your home directory.



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