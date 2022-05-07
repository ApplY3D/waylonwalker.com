---
canonical_url: https://waylonwalker.com/til/python-web-conf-snippet/
cover_image: https://images.waylonwalker.com/til/python-web-conf-snippet.png
description: ''
published: true
tags:
- python
title: python web conf snippet
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