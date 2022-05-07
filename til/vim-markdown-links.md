---
content: ''
cover: ''
date: 2022-03-19
datetime: 2022-03-19 00:00:00+00:00
description: Let Let Before you run someone Before you run someone Something that
  I have always appreciated form Something that I have always appreciated form Searchng
  throu
long_description: Let Let Before you run someone Before you run someone Something
  that I have always appreciated form Something that I have always appreciated form
  Searchng through the internet I was able to find an article from Searchng through
  the internet I was abl
now: 2022-05-07 21:32:25.891704
path: pages/til/vim-markdown-links.md
slug: til/vim-markdown-links
status: published
super_description: Let Let Before you run someone Before you run someone Something
  that I have always appreciated form Something that I have always appreciated form
  Searchng through the internet I was able to find an article from Searchng through
  the internet I was able to find an article from Here is my interpretation of the
  code I took from Vitaly Here is my interpretation of the code I took from Vitaly
  So far it is working for me and saving me a few seconds off each post I So far it
  is working for me and saving
tags:
- vim
- webdev
- meta
templateKey: til
title: Automatically Generate a list of Markown Links in Vim
today: 2022-05-07
year: 2022
---

Let's make a vim command to automatically collect all the links in these
posts at the end of each article.  Regex confuses the heck out of me...
I don't have my regex liscense, but
regex can be so darn powerful especially in an editor.

## Step one

Before you run someone's regex from the internet that you don't fully
understand, check your `git status` and make sure you are all clear with
git before you wreck something

## Inspiration

Something that I have always appreciated form
[Nick Janetakis](https://nickjanetakis.com/) is his links section.  I
often try to gather up the links at the end of my posts, but often end
up not doing it or forgetting.

## Making a Links section

Searchng through the internet I was able to find an article from
Vitaly Parnas called
[vim ref links](https://vitalyparnas.com/guides/vim-ref-links/) that did
almost exactly what I needed, except it was more complicated and made
them into ref liks.

Here is my interpretation of the code I took from Vitaly's post.  It
makes a Links section like the one at the bottom of this post.

``` vim
function! MdLinks()
    $norm o## Links
    $norm o
    g/\[[^\]]\+\]([^)]\+)/t$
    silent! '^,$s/\v[^\[]*(\[[^\]]+\])\(([^)]+)\)[^\[]*/* \1(\2)/g
    nohl
endfunction
command! MdLinks call MdLinks()
```

So far it is working for me and saving me a few seconds off each post I
make.

## Links

* [Nick Janetakis](https://nickjanetakis.com/)
* [vim ref links](https://vitalyparnas.com/guides/vim-ref-links/)