---
content: ''
cover: ''
date: 2020-01-01
datetime: 2020-01-01 00:00:00+00:00
description: Vim Vim Location List eating up the screen while I am zoomed in and trying
  to live code Location List eating up the screen while I am zoomed in and trying
  to li
long_description: 'Vim Vim Location List eating up the screen while I am zoomed in
  and trying to live code Location List eating up the screen while I am zoomed in
  and trying to live code Through some google search I found the culprit was syntastic.  It
  has an  Through '
now: 2022-05-07 21:32:25.894539
path: pages/blog/keep-location-list-closed.md
slug: keep-location-list-closed
status: published
super_description: 'Vim Vim Location List eating up the screen while I am zoomed in
  and trying to live code Location List eating up the screen while I am zoomed in
  and trying to live code Through some google search I found the culprit was syntastic.  It
  has an  Through some google search I found the culprit was syntastic.  It has an  I
  want to keep the location list open automatically most of the time, but when I don
  I want to keep the location list open automatically most of the time, but when I
  don First, create '
tags:
- vim
templateKey: blog-post
title: Keep Location List Closed
today: 2022-05-07
year: 2020
---

Vim's (neovim in my case) location list can provide some very useful information while developing.  Mine gives me information about linting and type checking errors with fairly little config.  Generally, it sits nicely at the bottom of the screen and barely affects me.  Other times, especially while zoomed way in during a presentation, it just gets in the way.

![location list eats the screen](https://images.waylonwalker.com/location-list-eats-screen.png)

> Location List eating up the screen while I am zoomed in and trying to live code

## Toggling the location list

Through some google search I found the culprit was syntastic.  It has an `auto_loc_list` feature.  We can turn it off by setting
`syntastic_auto_loc_list=0`.

``` vim
let syntastic_auto_loc_list=0
```

## Keybindings

I want to keep the location list open automatically most of the time, but when I don't want it to keep opening it's generally detrimental.  Trying to live code while the location list keeps taking up the whole screen is not cool.


First, create a function that will toggle both the location list and syntactic together.

``` vim
let s:syntastic_auto_loc_list = 0
function! s:ToggleLocationList()
    if s:syntastic_auto_loc_list == 1
        let s:syntastic_auto_loc_list = 0
        let syntastic_auto_loc_list = 0
        :lclose
    else
        let s:syntastic_auto_loc_list = 1
        let syntastic_auto_loc_list = 1
        :lopen
    endif
endfunction
```

This binding will allow me to use `gtl` from normal mode to toggle the location list.

``` vim
:command! ToggleLocationList :call s:ToggleLocationList()
nnoremap gtl :ToggleLocationList<CR>
```

I am starting a set of **toggle** keymaps under the `gt` keybinding, this one is the second one after a keybinding made to toggle paste mode.