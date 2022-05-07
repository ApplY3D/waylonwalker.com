---
Tags:
- cli
- linux
- tmux
content: ''
cover: ''
date: 2021-08-11
datetime: 2021-08-11 00:00:00+00:00
description: https://youtu.be/QWPyYx54JbE https://youtu.be/QWPyYx54JbE Now it Now
  it One viable option is to nuke the whole dang thing.  I actually do this more One
  viable o
long_description: 'https://youtu.be/QWPyYx54JbE https://youtu.be/QWPyYx54JbE Now it
  Now it One viable option is to nuke the whole dang thing.  I actually do this more
  One viable option is to nuke the whole dang thing.  I actually do this more save
  and commit your work '
now: 2022-05-07 21:32:25.892730
path: pages/blog/tmux-killing-tmux.md
slug: tmux-killing-tmux
status: published
super_description: https://youtu.be/QWPyYx54JbE https://youtu.be/QWPyYx54JbE Now it
  Now it One viable option is to nuke the whole dang thing.  I actually do this more
  One viable option is to nuke the whole dang thing.  I actually do this more save
  and commit your work diligently before  save and commit your work diligently before  A
  more reasonable option might be to kill a single session. A more reasonable option
  might be to kill a single session. Killing sessions one by one from the command
  line can be a bit ted
tags: []
templateKey: blog-post
title: killing tmux
today: 2022-05-07
year: 2021
---

https://youtu.be/QWPyYx54JbE

Now it's time to switch gears, we are onto a different part of our day and
there are just too many sessions running and we need to clean up shop.

## kill-server

One viable option is to nuke the whole dang thing.  I actually do this more
than you might think.

``` bash
tmux kill-server
```

> save and commit your work diligently before `kill-server`

## kill-session

A more reasonable option might be to kill a single session.

``` bash
# kills the current session
tmux kill-session

# kills the session named scratch
tmux kill-session -t scratch
```

## choose-tree

Killing sessions one by one from the command line can be a bit tedious, and
involve more keystrokes than necessary.  Another option built right into tmux
is `choose-tree`.  By default `choose-tree` is bound to `prefix+s`, that's
pressing control+b then s.  Once you are in `choose-tree`, you can navigate
around with your configured navigation scheme, press `x` to kill a session, or
pane or window then `y` to confirm.  You can also batch delete by tagging items
with t, and killing them all at once with `X`.


  <div class="onelinelink-wrapper">
      <a class="onelinelink" href="https://waylonwalker.com/tmux-choose-tree/">
          <img style="float: right;" align='right' src="https://images.waylonwalker.com/tmux-choose-tree-og_250x140.png" alt="article cover for 
 tmux choose-tree
"/>
          <p><strong>
 tmux choose-tree
</strong></p>
      </a>
  </div>


> check out this post for a bit more information on choose-tree

## fuzzy matcher

Here is my preferred way, using a fuzzy matcher.  I recently improved this one
by making it a popup and cleaning it up based on a repsonse,
[tmux-output-formatting](https://qmacro.org/autodidactics/2021/08/06/tmux-output-formatting/)
by [DJ Adams](https://twitter.com/qmacro).  I press prefix+k to bring up a kill-session menu.

``` bash
bind k display-popup -E "\
    tmux list-sessions -F '#{?session_attached,,#{session_name}}' |\
    fzf --reverse -m --header=kill-session |\
    xargs -I {} tmux kill-session -t {}"
```

> note this is setup to multiple sessions all at once.


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