---
canonical_url: https://waylonwalker.com/tmux-rotate-window/
cover_image: https://images.waylonwalker.com/tmux-rotate-window.png
description: https://youtu.be/06z5qf81ofo https://youtu.be/06z5qf81ofo Rotate window
  is the main way that I navigated tmux before I learned Rotate window is the main
  way tha
published: true
tags:
- cli
- linux
- tmux
title: tmux rotate-window
---

https://youtu.be/06z5qf81ofo

Rotate window is the main way that I navigated tmux before I learned
`select-pane`.  It allows you to change your focused pane, or rotate the
position of the panes easily.


Default keybindings

``` bash
bind-key        C-o rotate-window bind-key          o select-pane -t :.+
```

My keybindings look just a bit different than the default ones, I do not like needing to hit prefix for every command, especially for repeated commands.  I set a similar keybinding to the default one that uses mod instead of prefix.

``` bash
bind -n M-o select-pane -t :.+ bind -n M-O rotate-window
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