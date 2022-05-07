---
content: ''
cover: ''
date: 2022-02-14
datetime: 2022-02-14 00:00:00+00:00
description: Anyone just starting out their vim customization journey is bound to
  run into this error. Anyone just starting out their vim customization journey is
  bound to r
long_description: 'Anyone just starting out their vim customization journey is bound
  to run into this error. Anyone just starting out their vim customization journey
  is bound to run into this error. I I If you run  If you run  You still need to map
  your remaps with a :'
now: 2022-05-07 21:32:25.891362
path: pages/til/vim-cmd.md
slug: til/vim-cmd
status: published
super_description: 'Anyone just starting out their vim customization journey is bound
  to run into this error. Anyone just starting out their vim customization journey
  is bound to run into this error. I I If you run  If you run  You still need to map
  your remaps with a : if you do not close it with a You still need to map your remaps
  with a : if you do not close it with a If you can close the  If you can close the '
tags:
- vim
- linux
- cli
templateKey: til
title: 'Vim remaps use cmd in place of :'
today: 2022-05-07
year: 2022
---

Anyone just starting out their vim customization journey is bound to run into this error.

``` vim
E5520: <Cmd> mapping must end with <CR>
```

## I did not get it

I'll admit, in hindsight it's very clear what this is trying to tell me, but
for whatever reason I still did not understand it and I just used a :
everywhere.

## From the docs


If you run `:h <cmd>` you will see a lot of reasons why you should do it, from
performance, to hygene, to ergonomics.  You will also see another clear
statement about how to use `<cmd>`.

``` vim
                                                          E5520
  <Cmd> commands must terminate, that is, they must be followed by <CR> in the
  {rhs} of the mapping definition.  Command-line mode is never entered.
```

## When to map with a :

You still need to map your remaps with a : if you do not close it with a
`<cr>`.  This might be something like prefilling a command with a search term.

``` vim
nnoremap <leader><leader>f :s/search/
```

## Otherwise use <cmd>

If you can close the `<cmd>` with a `<cr>` the command do so.  Your map will
automatically be silent, more ergonomic, performant, and all that good stuff.

``` vim
nnoremap <leader><leader>f <cmd>s/search/Search/g<cr>
```