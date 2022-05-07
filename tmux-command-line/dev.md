---
canonical_url: https://waylonwalker.com/tmux-command-line/
cover_image: https://images.waylonwalker.com/tmux-command-line.png
description: https://youtu.be/SNu-4IrkjAs https://youtu.be/SNu-4IrkjAs So far we have
  covered a lot of tmux commands and how they map to keybindings So far we have covered
  a
published: true
tags:
- cli
- linux
- tmux
title: tmux command line
---

https://youtu.be/SNu-4IrkjAs

So far we have covered a lot of tmux commands and how they map to keybindings but these same commands can be executed at the command line.

## From the command line

Let's make a popup that displays our git status for 5s or until we close it manually.  We can run the following command at the command line, in a split.

``` bash
tmux display-popup -E -d '#{pane_current_path}' 'git status && sleep 5'
```

## From the tmux command line

Or we can open the tmux command line and run it from tmux's built in command line, which is very similar to bim EX mode. By default the tmux command line can be opened with `prefix+[`.

``` bash
display-popup -E -d '#{pane_current_path}' 'git status && sleep 5'
```
> 🗒️ note that the tmux command is called by default when inside of tmux.

## Make it a keybinding

Finally we can make it a keybinding by adding a bind command ahead of our tmux command, then we can execute this in the tmux command line or add it to our
`~/.tmux.conf`.

``` bash
bind s display-popup -E -d '#{pane_current_path}' 'git status && sleep 5'
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