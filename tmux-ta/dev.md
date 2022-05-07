---
canonical_url: https://waylonwalker.com/tmux-ta/
cover_image: https://images.waylonwalker.com/tmux-ta.png
description: https://youtu.be/nT0FA1RNZEs https://youtu.be/nT0FA1RNZEs Now your creating,
  jumping, and killing sessions like a boss. You are slicing Now your creating, jumpi
published: true
tags: []
title: tmux ta
---

https://youtu.be/nT0FA1RNZEs

Now your creating, jumping, and killing sessions like a boss. You are slicing through projects with ease, let me show you one more thing that can be the cream on top of this silky smooth setup we have been working towards.

## [Chris Toomey's](https://twitter.com/christoomey) Tmux Course

This script is simply my fork of Chris Toomey's `tat` script straight out of his course.  It helps us create or jump to project specific sessions with ease.

## a directory of projects

My version of the `ta` script will let you pass it a directory, and it will give you a fuzzy popup.

``` bash
ta ~/git
```

## setting up a keybinding

``` bash
bind C-g display-popup -E "ta ~/git"
```

![ta-git](https://images.waylonwalker.com/ta-git.png)

## default layout

By default I have my projects open with a vertical split, vim is on top, with my file finder open and the lower split is set to just my terminal.  This is what I do 90% of the time that I open a project anyways.

![ta-git-layout](https://images.waylonwalker.com/ta-git-layout.png)

## More projects

I also have a directory setup that is a symlink-gallery of all of my projects, both private and public.  This makes it easy to have one key that lets me see all of my projects.

```bash
rm -rf ~/projects mkdir ~/projects ln -sf ~/work/* ~/projects ln -sf ~/git/* ~/projects
```


  <div class="onelinelink-wrapper">
      <a class="onelinelink" href="https://waylonwalker.com/symlink-gallery/">
          <img style="float: right;" align='right' src="https://images.waylonwalker.com/symlink-gallery-og_250x140.png" alt="article cover for 
 Create a Virtual File Gallery with Symlinks
"/>
          <p><strong>
 Create a Virtual File Gallery with Symlinks
</strong></p>
      </a>
  </div>


> This post covers how I combine all my projects into a single directory.

## Related Links

* [default key bindings](https://gist.github.com/mzmonsour/8791835)
* [Chris Toomey's](https://twitter.com/christoomey) Tmux Course
* my [ta script](https://github.com/WaylonWalker/devtainer/blob/main/bin/.local/bin/ta)
* my [.tmux.conf](https://github.com/WaylonWalker/devtainer/blob/main/tmux/.tmux.conf)


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