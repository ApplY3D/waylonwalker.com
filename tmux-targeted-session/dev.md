---
canonical_url: https://waylonwalker.com/tmux-targeted-session/
cover_image: https://images.waylonwalker.com/tmux-targeted-session.png
description: https://youtu.be/5KE7Il7SOEk https://youtu.be/5KE7Il7SOEk This is something
  that I made up but use every single day, this is what keeps This is something that
  I
published: true
tags: []
title: tmux targeted session
---

https://youtu.be/5KE7Il7SOEk

This is something that I made up but use every single day, this is what keeps much of what is on my blog or my teams private work wiki going.  I have a few very important directories that I have assigned directly to a hotkey for fast session switching.

``` bash
bind -n M-i new-session -A -s waylonwalker_com "cd ~/git/waylonwalker.com/ && nvim" bind i popup -E -h 95% -w 95% -x 100% "tmux new-session -A -s waylonwalker_com 'cd ~/git/waylonwalker.com/ && nvim'" bind -n M-I popup -E "tmux new-session -A -s waylonwalker_com 'cd ~/git/waylonwalker.com/ && nvim'"
```


  <div class="onelinelink-wrapper">
      <a class="onelinelink" href="https://waylonwalker.com/tmux-new-session/">
          <img style="float: right;" align='right' src="https://images.waylonwalker.com/tmux-new-session-og_250x140.png" alt="article cover for 
 tmux new-session
"/>
          <p><strong>
 tmux new-session
</strong></p>
      </a>
  </div>


> This one is building off of yeserday's new-session post, make sure you check that one out as well.


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