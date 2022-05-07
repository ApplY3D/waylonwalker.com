---
canonical_url: https://waylonwalker.com/tmux-join-pane/
cover_image: https://images.waylonwalker.com/tmux-join-pane.png
description: https://youtu.be/Vm5rRtcVXLw https://youtu.be/Vm5rRtcVXLw Join-pane allows
  you to join panes that you have broken away from your window, Join-pane allows you
  to
published: true
tags:
- cli
- linux
- tmux
title: tmux join-pane
---

https://youtu.be/Vm5rRtcVXLw

Join-pane allows you to join panes that you have broken away from your window, or created in a different window to the window you want it in.  As far as I know there is not a default keybinding for it.

Before you can join a pane you must first have a pane marked to join.  Once you mark a pane, go back to the window you want to join it to and join-pane.

My keybindings, you must add this to your `~/.tmux.conf` file to use them.

``` python
# Mark and swap panes
#――――――――――――――――――――――――――――――――――――――――――――
bind -n M-m select-pane -m # mark bind -n M-M select-pane -M # unmark

bind -n M-< join-pane
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

Also check out the full YouTube [tmux-playlist](https://www.youtube.com/playlist?list=PLTRNG6WIHETB4reAxbWza3CZeP9KL6Bkr) to see all of the videos in this series.