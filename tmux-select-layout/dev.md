---
canonical_url: https://waylonwalker.com/tmux-select-layout/
cover_image: https://images.waylonwalker.com/tmux-select-layout.png
description: https://youtu.be/F0mHnwTrNNc https://youtu.be/F0mHnwTrNNc When you get
  many splits going in tmux sometimes its time for a new layout. When you get many
  splits g
published: true
tags:
- cli
- linux
- tmux
title: tmux select-layout
---

https://youtu.be/F0mHnwTrNNc

When you get many splits going in tmux sometimes its time for a new layout. There are four layout strategies that I use, main-vertical, main-horizontal, even-vertical, even-horizontal. Almost always I am useing the main ones with mod plus a or mod plus shift a keybindings.

``` bash
# Select Layouts
#―――――――――――――――――
bind -n M-a select-layout main-vertical bind -n M-A select-layout main-horizontal  bind -n M-E select-layout even-vertical bind -n M-V select-layout even-horizontal
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