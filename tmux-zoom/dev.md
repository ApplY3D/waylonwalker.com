---
canonical_url: https://waylonwalker.com/tmux-zoom/
cover_image: https://images.waylonwalker.com/tmux-zoom.png
description: https://youtu.be/Rn6mOarCQ-Y https://youtu.be/Rn6mOarCQ-Y Zooming into
  the current split in tmux is a valuable tool to give yourself some Zooming into
  the curre
published: true
tags:
- cli
- linux
- tmux
title: tmux zoom
---

https://youtu.be/Rn6mOarCQ-Y

Zooming into the current split in tmux is a valuable tool to give yourself some screen real estate.  These days I am almost always presenting, streaming, or pairing up with a co-worker over a video call.  Since I am always sharing my screen I am generally zoomed in to a level that is just a bit uncomfortable, so anytime I make a split it is really uncomfortable, being able to zoom into the split I am focused on is a big help, and also help anyone watching follow where I am currently working.


Default key bindings for zooming the current split

``` bash
bind-key          z resize-pane -Z
```


I have rebound this to match the default binding with mod+z rather so that I get that single keystroke experience.

``` bash
bind -n M-z resize-pane -Z
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