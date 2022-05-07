---
content: ''
cover: ''
date: 2021-07-22
datetime: 2021-07-22 00:00:00+00:00
description: https://youtu.be/06z5qf81ofo https://youtu.be/06z5qf81ofo Rotate window
  is the main way that I navigated tmux before I learned Rotate window is the main
  way tha
long_description: https://youtu.be/06z5qf81ofo https://youtu.be/06z5qf81ofo Rotate
  window is the main way that I navigated tmux before I learned Rotate window is the
  main way that I navigated tmux before I learned Default keybindings Default keybindings
  My keybindings
now: 2022-05-07 21:32:25.892683
path: pages/blog/tmux-rotate-window.md
slug: tmux-rotate-window
status: published
super_description: 'https://youtu.be/06z5qf81ofo https://youtu.be/06z5qf81ofo Rotate
  window is the main way that I navigated tmux before I learned Rotate window is the
  main way that I navigated tmux before I learned Default keybindings Default keybindings
  My keybindings look just a bit different than the default ones, I do not like My
  keybindings look just a bit different than the default ones, I do not like https://waylonwalker.com/tmux-nav-2021/
  https://waylonwalker.com/tmux-nav-2021/ for more information on how '
tags:
- cli
- linux
- tmux
templateKey: blog-post
title: tmux rotate-window
today: 2022-05-07
year: 2021
---

https://youtu.be/06z5qf81ofo

Rotate window is the main way that I navigated tmux before I learned
`select-pane`.  It allows you to change your focused pane, or rotate the
position of the panes easily.


Default keybindings

``` bash
bind-key        C-o rotate-window
bind-key          o select-pane -t :.+
```

My keybindings look just a bit different than the default ones, I do not like
needing to hit prefix for every command, especially for repeated commands.  I
set a similar keybinding to the default one that uses mod instead of prefix.

``` bash
bind -n M-o select-pane -t :.+
bind -n M-O rotate-window
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