---
canonical_url: https://waylonwalker.com/til/nvim-rename-python/
cover_image: https://images.waylonwalker.com/til/nvim-rename-python.png
description: I don I don I first tried the nvim lsp rename, and it failed, Then I
  pip installed I first tried the nvim lsp rename, and it failed, Then I pip installed
  Once y
published: true
tags:
- python
- vim
- vim
title: Rename Python Variables with nvim
---

I don't use refactoring tools as much as I probably should.  mostly because I work with small functions with unique names, but I recently had a case where a variable name `m` was everywhere and I wanted it named better.  This was not possible with find and replace, because there were other `m`'s in this region.


I first tried the nvim lsp rename, and it failed, Then I pip installed rope, a refactoring tool for python, and it just worked!

```bash
pip install rope
```

Once you have rope installed you can call rename on the variable.

```vim
:lua vim.lsp.buf.rename()
```