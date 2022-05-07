---
content: ''
cover: ''
date: 2021-06-25
datetime: 2021-06-25 00:00:00+00:00
description: Git can be a bit tricky to get configured correctly.  I often stumble
  into Git can be a bit tricky to get configured correctly.  I often stumble into
long_description: Git can be a bit tricky to get configured correctly.  I often stumble
  into Git can be a bit tricky to get configured correctly.  I often stumble into
now: 2022-05-07 21:32:25.894312
path: pages/blog/git-settings.md
slug: git-settings
status: draft
super_description: Git can be a bit tricky to get configured correctly.  I often stumble
  into Git can be a bit tricky to get configured correctly.  I often stumble into
tags:
- git
- linux
templateKey: blog-post
title: How I configure git
today: 2022-05-07
year: 2021
---

Git can be a bit tricky to get configured correctly.  I often stumble into
config issues weeks after setting up a new machine that I did not even notice.
These are my notes to remind me how I configure git.

## Identity

``` bash
git config --global user.name "John Doe"
git config --global user.email johndoe@example.com
```

## rebase


## editor


``` bash
git config --global core.editor nvim
```


## default branch


``` bash
git config --global init.defaultBranch main
```

## push to current bransh wihtout setting upstream

``` bash
git config --global push.default current
```

## Autostash

``` bash
git config pull.rebase true
git config rebase.autoStash true
```