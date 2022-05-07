---
content: ''
cover: ''
date: 2022-01-19
datetime: 2022-01-19 00:00:00+00:00
description: I really appreciate that in linux anything can be scripted, including
  I really appreciate that in linux anything can be scripted, including I set my default
  wal
long_description: 'I really appreciate that in linux anything can be scripted, including
  I really appreciate that in linux anything can be scripted, including I set my default
  wallpaper with  I set my default wallpaper with  Leaning in on feh, we can use fzf
  to pick a '
now: 2022-05-07 21:32:25.891973
path: pages/til/fzf-wallpaper.md
slug: til/fzf-wallpaper
status: published
super_description: I really appreciate that in linux anything can be scripted, including
  I really appreciate that in linux anything can be scripted, including I set my default
  wallpaper with  I set my default wallpaper with  Leaning in on feh, we can use fzf
  to pick a wallpaper from a directory Leaning in on feh, we can use fzf to pick a
  wallpaper from a directory I have mine alias I have mine alias
tags:
- linux
- cli
- bash
templateKey: til
title: fuzzy wallpaper with fzf
today: 2022-05-07
year: 2022
---

I really appreciate that in linux anything can be scripted, including
setting the wallpaper.  So everytime I disconnect a monitor I can just
rerun my script and fix my wallpaper without digging deep into the ui
and fussing through a bunch of settings.

``` bash
feh --bg-scale ~/.config/awesome/wallpaper/my_wallpaper.png
```

> I set my default wallpaper with `feh` using the command above.

Leaning in on feh, we can use fzf to pick a wallpaper from a directory
full of wallpapers with very few keystrokes.

```
alias wallpaper='ls ~/.config/awesome/wallpaper | fzf --preview="feh --bg-scale ~/.config/awesome/wallpaper/{}" | xargs -I {} feh --bg-scale ~/.config/awesome/wallpaper/{}'
```

> I have mine alias'd to `wallpaper` so that I can quickly run it from
> my terminal.