---
content: ''
cover: ''
date: 2022-02-18
datetime: 2022-02-18 00:00:00+00:00
description: Glances is a fully featured system monitoring tool written in python.  Out
  of Glances is a fully featured system monitoring tool written in python.  Out of
  Once
long_description: Glances is a fully featured system monitoring tool written in python.  Out
  of Glances is a fully featured system monitoring tool written in python.  Out of
  Once you run this you will be in a tui application similar to htop.  You can Once
  you run this
now: 2022-05-07 21:32:25.891424
path: pages/til/pipx-run-glances.md
slug: til/pipx-run-glances
status: published
super_description: Glances is a fully featured system monitoring tool written in python.  Out
  of Glances is a fully featured system monitoring tool written in python.  Out of
  Once you run this you will be in a tui application similar to htop.  You can Once
  you run this you will be in a tui application similar to htop.  You can
tags:
- python
templateKey: til
title: Run glances without install with pipx
today: 2022-05-07
year: 2022
---

Glances is a fully featured system monitoring tool written in python.  Out of
the box it's quite similar to htop, but has quite a few more features, and can
be ran without installing anything other than `pipx`, which you should already
have installed if you do anything with python.


``` bash
pipx run glances
```

Once you run this you will be in a tui application similar to htop.  You can
kill processes with k, use left and right arrows to change the sorting column,
and up and down to select different processes.

![running pipx run glances on my ubuntu 21.10 machine inside the kitty terminal](https://images.waylonwalker.com/pipx-run-glances.png)

## Links

* [pipx](https://pypa.github.io/pipx/)
* [website](https://nicolargo.github.io/glances/)
* [docs](https://glances.readthedocs.io/en/latest/index.html)
* [github](https://github.com/nicolargo/glances)