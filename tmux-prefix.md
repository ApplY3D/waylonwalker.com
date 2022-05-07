---
content: ''
cover: ''
date: 2021-07-18
datetime: 2021-07-18 00:00:00+00:00
description: https://youtu.be/BMkpbfhbkKM https://youtu.be/BMkpbfhbkKM The prefix
  key is an essential part of tmux, by default all of tmux The prefix key is an essential
  par
long_description: https://youtu.be/BMkpbfhbkKM https://youtu.be/BMkpbfhbkKM The prefix
  key is an essential part of tmux, by default all of tmux The prefix key is an essential
  part of tmux, by default all of tmux A few of the essential default key-bindings.
  A few of th
now: 2022-05-07 21:32:25.894076
path: pages/blog/tmux-prefix.md
slug: tmux-prefix
status: published
super_description: https://youtu.be/BMkpbfhbkKM https://youtu.be/BMkpbfhbkKM The prefix
  key is an essential part of tmux, by default all of tmux The prefix key is an essential
  part of tmux, by default all of tmux A few of the essential default key-bindings.
  A few of the essential default key-bindings. A more complete list of key-bindings
  can be found in this gist https://gist.github.com/mzmonsour/8791835. A more complete
  list of key-bindings can be found in this gist https://gist.github.com/mzmonsour/8791835.
  http
tags:
- cli
- linux
- tmux
templateKey: blog-post
title: tmux prefix
today: 2022-05-07
year: 2021
---

https://youtu.be/BMkpbfhbkKM

The prefix key is an essential part of tmux, by default all of tmux's
key-bindings sit behind a prefix.  This prefix is very similar to vim's leader
key. It is common for folks to change the default `C-b` (control b) to `C-a` or
if they are a vim user something to match their vim leader key.

``` bash
set -g prefix C-Space
bind Space send-prefix
```

A few of the essential default key-bindings.

```
%      vertical split
"      horizontal split
d      detach

up     select up one pane
down   select down one pane
right  select right one pane
left   select left one pane

t      clock
o      swap panes
c      create window
n      next window
p      previous window
```

A more complete list of key-bindings can be found in this gist https://gist.github.com/mzmonsour/8791835.


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