---
content: ''
cover: ''
date: 2100-03-20
datetime: 2100-03-20 00:00:00+00:00
description: ''
long_description: ''
now: 2022-05-07 21:32:25.891824
path: pages/til/python-web-conf-snippet.md
slug: til/python-web-conf-snippet
status: draft
super_description: ''
tags:
- python
templateKey: til
title: python web conf snippet
today: 2022-05-07
year: 2100
---

## From my terminal

``` bash
pipx run \
 --spec git+https://github.com/waylonwalker/lookatme \
 lookatme {filepath} \
 --live-reload \
 --style gruvbox-dark
```

## From Neovim

``` vim
nnoremap <leader><leader>s <cmd>lua require'telegraph'.telegraph({cmd='pipx run --spec git+https://github.com/waylonwalker/lookatme lookatme {filepath} --live-reload --style gruvbox-dark', how='tmux'})<CR>
```