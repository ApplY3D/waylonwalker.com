---
content: ''
cover: ''
date: 2022-01-16
datetime: 2022-01-16 00:00:00+00:00
description: I don I don I first tried the nvim lsp rename, and it failed, Then I
  pip installed I first tried the nvim lsp rename, and it failed, Then I pip installed
  Once y
long_description: I don I don I first tried the nvim lsp rename, and it failed, Then
  I pip installed I first tried the nvim lsp rename, and it failed, Then I pip installed
  Once you have rope installed you can call rename on the variable. Once you have
  rope installed y
now: 2022-05-07 21:32:25.891905
path: pages/til/nvim-rename-python.md
slug: til/nvim-rename-python
status: published
super_description: I don I don I first tried the nvim lsp rename, and it failed, Then
  I pip installed I first tried the nvim lsp rename, and it failed, Then I pip installed
  Once you have rope installed you can call rename on the variable. Once you have
  rope installed you can call rename on the variable.
tags:
- python
- vim
- vim
templateKey: til
title: Rename Python Variables with nvim
today: 2022-05-07
year: 2022
---

I don't use refactoring tools as much as I probably should.  mostly
because I work with small functions with unique names, but I recently
had a case where a variable name `m` was everywhere and I wanted it
named better.  This was not possible with find and replace, because
there were other `m`'s in this region.


I first tried the nvim lsp rename, and it failed, Then I pip installed
rope, a refactoring tool for python, and it just worked!

```bash
pip install rope
```

Once you have rope installed you can call rename on the variable.

```vim
:lua vim.lsp.buf.rename()
```