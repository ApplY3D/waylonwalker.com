---
canonical_url: https://waylonwalker.com/til/remove-vim-tab-characters/
cover_image: https://images.waylonwalker.com/til/remove-vim-tab-characters.png
description: I I It turns out they are tabs, and you can get rid of the little leading
  It turns out they are tabs, and you can get rid of the little leading
published: true
tags:
- vim
- linux
title: Remove Vim Tab Characters
---

I've been stuck many times looking at a vim buffer with little question marks at the beginning of each line and trying to get rid of them.  for so long I didn't know what they were so trying to get rid of them was impossible.

![example of what the tab character renders as in my editor](https://images.waylonwalker.com/vim-tab-characters.png)

It turns out they are tabs, and you can get rid of the little leading question marks with this substitution command.

``` vim
:%s/\t/    /g
```