---
content: ''
cover: ''
date: 2021-05-17
datetime: 2021-05-17 00:00:00+00:00
description: Setting up python with the native nvim>0.5 lsp was mr Setting up python
  with the native nvim>0.5 lsp was mr https://github.com/neovim/nvim-lspconfig https://git
long_description: Setting up python with the native nvim>0.5 lsp was mr Setting up
  python with the native nvim>0.5 lsp was mr https://github.com/neovim/nvim-lspconfig
  https://github.com/neovim/nvim-lspconfig https://github.com/palantir/python-language-server/issues/19
now: 2022-05-07 21:32:25.893235
path: pages/blog/setup-pylsp.md
slug: setup-pylsp
status: draft
super_description: Setting up python with the native nvim>0.5 lsp was mr Setting up
  python with the native nvim>0.5 lsp was mr https://github.com/neovim/nvim-lspconfig
  https://github.com/neovim/nvim-lspconfig https://github.com/palantir/python-language-server/issues/190
  https://github.com/palantir/python-language-server/issues/190 Getting mypy working
  with lsp was tricky for me.  I had some issues trying to Getting mypy working with
  lsp was tricky for me.  I had some issues trying to
tags:
- vim
- linux
- python
templateKey: blog-post
title: python lsp setup
today: 2022-05-07
year: 2021
---

Setting up python with the native nvim>0.5 lsp was mr


## lsp-config

https://github.com/neovim/nvim-lspconfig

``` vim
lua << EOF
require'lspconfig'.pyright.setup{}
EOF
```

## pyls#190

https://github.com/palantir/python-language-server/issues/190

``` lua
lspconfig.pyls.setup {
  cmd = {"pyls"},
  filetypes = {"python"},
  settings = {
    pyls = {
      configurationSources = {"flake8"},
      plugins = {
        jedi_completion = {enabled = true},
        jedi_hover = {enabled = true},
        jedi_references = {enabled = true},
        jedi_signature_help = {enabled = true},
        jedi_symbols = {enabled = true, all_scopes = true},
        pycodestyle = {enabled = false},
        flake8 = {
          enabled = true,
          ignore = {},
          maxLineLength = 160
        },
        mypy = {enabled = false},
        isort = {enabled = false},
        yapf = {enabled = false},
        pylint = {enabled = false},
        pydocstyle = {enabled = false},
        mccabe = {enabled = false},
        preload = {enabled = false},
        rope_completion = {enabled = false}
      }
    }
  },
  on_attach = on_attach
}
```


## mypy

Getting mypy working with lsp was tricky for me.  I had some issues trying to
run mypy in ci and pyright in my editor and I really wanted them to match.

``` bash
pipx install 'python-lsp-server[all]'
pipx inject python-lsp-server pylsp-mypy
```