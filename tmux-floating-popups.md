---
content: ''
cover: ''
date: 2021-07-15
datetime: 2021-07-15 00:00:00+00:00
description: https://youtu.be/2ZqFDsJywt8 https://youtu.be/2ZqFDsJywt8 Tmux popups
  are actually floating windows that you can drag around the screen.  They always
  open in th
long_description: 'https://youtu.be/2ZqFDsJywt8 https://youtu.be/2ZqFDsJywt8 Tmux
  popups are actually floating windows that you can drag around the screen.  They
  always open in the middle (by default) when you open them, no matter where you leave
  them. Tmux popups are '
now: 2022-05-07 21:32:25.894403
path: pages/blog/tmux-floating-popups.md
slug: tmux-floating-popups
status: published
super_description: https://youtu.be/2ZqFDsJywt8 https://youtu.be/2ZqFDsJywt8 Tmux
  popups are actually floating windows that you can drag around the screen.  They
  always open in the middle (by default) when you open them, no matter where you leave
  them. Tmux popups are actually floating windows that you can drag around the screen.  They
  always open in the middle (by default) when you open them, no matter where you leave
  them. Here are a couple of keybindings I use to open up popup windows. Here are
  a couple of keyb
tags:
- cli
- linux
- tmux
templateKey: blog-post
title: tmux floating popups
today: 2022-05-07
year: 2021
---

https://youtu.be/2ZqFDsJywt8

Tmux popups are actually floating windows that you can drag around the screen.  They always open in the middle (by default) when you open them, no matter where you leave them.

Here are a couple of keybindings I use to open up popup windows.

``` bash
bind C-g display-popup -E "ta ~/git"
bind -n M-g display-popup -E "tmux new-session -A -s scratch"
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