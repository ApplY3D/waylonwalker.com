---
Tags:
- cli
- linux
- tmux
content: ''
cover: ''
date: 2021-08-06
datetime: 2021-08-06 00:00:00+00:00
description: https://youtu.be/dDq0depPrTs https://youtu.be/dDq0depPrTs So you have
  been tricking out that  So you have been tricking out that  Let Let We can run this
  comman
long_description: https://youtu.be/dDq0depPrTs https://youtu.be/dDq0depPrTs So you
  have been tricking out that  So you have been tricking out that  Let Let We can
  run this command from your shell to re-source your changed  We can run this command
  from your shell to re
now: 2022-05-07 21:32:25.894268
path: pages/blog/tmux-source-file.md
slug: tmux-source-file
status: published
super_description: https://youtu.be/dDq0depPrTs https://youtu.be/dDq0depPrTs So you
  have been tricking out that  So you have been tricking out that  Let Let We can
  run this command from your shell to re-source your changed  We can run this command
  from your shell to re-source your changed  It also works from the tmux command line.
  It also works from the tmux command line. It It This is my preferred way of re-sourcing
  my  This is my preferred way of re-sourcing my  https://waylonwalker.com/tmux-nav-2021/
  https://wa
tags: []
templateKey: blog-post
title: tmux source-file
today: 2022-05-07
year: 2021
---

https://youtu.be/dDq0depPrTs

So you have been tricking out that `.tmux.conf`, you're looking for a silky
smooth workflow that lets you fly through tmux with super speed, but every time
you tweak out that `.tmux.conf` you have to restart your whole session. Not amymore,

Let's add this to the bottom of our tmux.conf so that you can see everytime it
gets sourced.

``` bash
display-message "hello beautiful"
```

## command

We can run this command from your shell to re-source your changed `.tmux.conf`

``` bash
tmux source-file ~/.tmux.conf
```

It also works from the tmux command line.

``` bash
source-file ~/.tmux.conf
```


## tmux hotkey

It's very common to set this up as a keybinding so that you can do it easily
without needing to memorize the exact command.

``` bash
bind -T prefix r source-file ~/.tmux.conf
bind -n M-r source-file ~/.tmux.conf
```

## from vim

This is my preferred way of re-sourcing my `.tmux.conf`.  It sits quietly in
the background, and I dont need to remember to do anything.  If you are a vim
user you can automate this process by creating a `autocmd bufwritepost`.  This
will shell out the `tmux source-file` everytime you save your `.tmux.conf`.

``` vim
autocmd bufwritepost .tmux.conf execute ':!tmux source-file %'
autocmd bufwritepost .tmux.local.conf execute ':!tmux source-file %'
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