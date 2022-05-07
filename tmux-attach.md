---
content: ''
cover: ''
date: 2021-07-31
datetime: 2021-07-31 00:00:00+00:00
description: https://youtu.be/JQ0yDCVu44E https://youtu.be/JQ0yDCVu44E attach is one
  of the most useful features of tmux.  If you have no interest in attach is one of
  the mo
long_description: https://youtu.be/JQ0yDCVu44E https://youtu.be/JQ0yDCVu44E attach
  is one of the most useful features of tmux.  If you have no interest in attach is
  one of the most useful features of tmux.  If you have no interest in this command
  will simply attach ba
now: 2022-05-07 21:32:25.894680
path: pages/blog/tmux-attach.md
slug: tmux-attach
status: published
super_description: https://youtu.be/JQ0yDCVu44E https://youtu.be/JQ0yDCVu44E attach
  is one of the most useful features of tmux.  If you have no interest in attach is
  one of the most useful features of tmux.  If you have no interest in this command
  will simply attach back to tmux if you are ever disconnected this command will simply
  attach back to tmux if you are ever disconnected If you ever run long running tasks
  on a remote machine by sshing into this you If you ever run long running tasks on
  a remote machine by
tags:
- cli
- linux
- tmux
templateKey: blog-post
title: tmux attach
today: 2022-05-07
year: 2021
---

https://youtu.be/JQ0yDCVu44E

attach is one of the most useful features of tmux.  If you have no interest in
tmux for pane and window management, you should use tmux for this.  It can be a
life saver if you ever get disconnected from the host machine or accidently
close your terminal you can connect right back into the session you were just
in using attach.

## attach

``` bash
tmux attach
```

> this command will simply attach back to tmux if you are ever disconnected

If you ever run long running tasks on a remote machine by sshing into this you
should be doing it inside tmux, or something like tmux so that you do not loose
your work.

## attach to a specific session

If you have multiple sessions running you can select the session that you want
to attach to by passing `-t <name-of-session>`.

``` bash
tmux attach -t scratch
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