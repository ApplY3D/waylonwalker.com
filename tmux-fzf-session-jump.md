---
Tags:
- cli
- linux
- tmux
content: ''
cover: ''
date: 2021-08-05
datetime: 2021-08-05 00:00:00+00:00
description: https://youtu.be/DkJ9rb85LC0 https://youtu.be/DkJ9rb85LC0 Quickly getting
  between tmux splits is critical skill for productivity.  You Quickly getting between
  t
long_description: https://youtu.be/DkJ9rb85LC0 https://youtu.be/DkJ9rb85LC0 Quickly
  getting between tmux splits is critical skill for productivity.  You Quickly getting
  between tmux splits is critical skill for productivity.  You I have used this fzf
  one keybinding fo
now: 2022-05-07 21:32:25.894651
path: pages/blog/tmux-fzf-session-jump.md
slug: tmux-fzf-session-jump
status: published
super_description: 'https://youtu.be/DkJ9rb85LC0 https://youtu.be/DkJ9rb85LC0 Quickly
  getting between tmux splits is critical skill for productivity.  You Quickly getting
  between tmux splits is critical skill for productivity.  You I have used this fzf
  one keybinding for quite awhile,  honestly I did not make I have used this fzf one
  keybinding for quite awhile,  honestly I did not make Like with many of my keybindings
  I have swapped this one out for a popup Like with many of my keybindings I have
  swapped this one '
tags: []
templateKey: blog-post
title: tmux fzf session jumper
today: 2022-05-07
year: 2021
---

https://youtu.be/DkJ9rb85LC0

Quickly getting between tmux splits is critical skill for productivity.  You
can get by with `next` or `prev` session for awhile, but if you have more than
about three session you need something a bit more targeted.


## Full Screen selector

I have used this fzf one keybinding for quite awhile,  honestly I did not make
it up, and cannot remember where it came from. It will open up a session picker
in a new full screen window.

``` bash
bind C-j new-window -n "session-switcher" "tmux list-sessions | sed -E 's/:.*$//' | grep -v \"^$(tmux display-message -p '#S')\$\" | fzf --reverse | xargs tmux switch-client -t"
```

## Popup selector

Like with many of my keybindings I have swapped this one out for a popup
version.  It just feels so smooth.

``` bash
bind C-j display-popup -E "tmux list-sessions | sed -E 's/:.*$//' | grep -v \"^$(tmux display-message -p '#S')\$\" | fzf --reverse | xargs tmux switch-client -t"
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


Also check out the full YouTube
[tmux-playlist](https://www.youtube.com/playlist?list=PLTRNG6WIHETB4reAxbWza3CZeP9KL6Bkr)
to see all of the videos in this series.