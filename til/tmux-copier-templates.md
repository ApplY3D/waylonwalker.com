---
content: ''
cover: ''
date: 2022-01-24
datetime: 2022-01-24 00:00:00+00:00
description: I have added a hotkey to my copier template setup to quickly access all
  my I have added a hotkey to my copier template setup to quickly access all my I
  I
long_description: I have added a hotkey to my copier template setup to quickly access
  all my I have added a hotkey to my copier template setup to quickly access all my
  I I
now: 2022-05-07 21:32:25.892025
path: pages/til/tmux-copier-templates.md
slug: til/tmux-copier-templates
status: published
super_description: I have added a hotkey to my copier template setup to quickly access
  all my I have added a hotkey to my copier template setup to quickly access all my
  I I
tags:
- python
- linux
- tmux
templateKey: til
title: Tmux hotkey for copier templates
today: 2022-05-07
year: 2022
---

I have added a hotkey to my copier template setup to quickly access all my
templates at any time from tmux.  At any point I can hit `<c-b><c-b>`, thats
holding control and hitting `bb`, and I will get a popup list of all of my
templates directory names.  Its an fzf list, which means that I can fuzzy
search through it for the template I want, or arrow key to the one I want if I
am feeling insane.  I even setup it up so that the preview is a list of the
files that come with the template in tree view.

``` bash
bind-key c-b popup -E -w 80% -d '#{pane_current_path}' "\
    pipx run copier copy ~/.copier-templates/`ls ~/.copier-templates |\
    fzf --header $(pwd) --preview='tree ~/.copier-templates/{} |\
    lolcat'` . \
    "
```

I've had this on my systems for a few weeks now and I am constantly using it
for my [tils](https://waylonwalker.com/til/),
[blogs](https://waylonwalker.com/archive), and my .envrc file that goes into
all of my projects to make sure that I have a virtual environment installed and
running any time I open it.

![this is what it looks like when I open my copier templates popup](https://images.waylonwalker.com/copier-templates-tmux-popup.png)