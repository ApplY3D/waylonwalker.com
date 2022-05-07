---
canonical_url: https://waylonwalker.com/tmux-floating-popups/
cover_image: https://images.waylonwalker.com/tmux-floating-popups.png
description: https://youtu.be/2ZqFDsJywt8 https://youtu.be/2ZqFDsJywt8 Tmux popups
  are actually floating windows that you can drag around the screen.  They always
  open in th
published: true
tags:
- cli
- linux
- tmux
title: tmux floating popups
---

https://youtu.be/2ZqFDsJywt8

Tmux popups are actually floating windows that you can drag around the screen.  They always open in the middle (by default) when you open them, no matter where you leave them.

Here are a couple of keybindings I use to open up popup windows.

``` bash
bind C-g display-popup -E "ta ~/git" bind -n M-g display-popup -E "tmux new-session -A -s scratch"
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