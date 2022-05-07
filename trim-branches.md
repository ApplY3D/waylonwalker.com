---
content: ''
cover: ''
date: 2021-05-07
datetime: 2021-05-07 00:00:00+00:00
description: ''
long_description: ''
now: 2022-05-07 21:32:25.893521
path: pages/blog/trim-branches.md
slug: trim-branches
status: published
super_description: ''
tags:
- git
- bash
- linux
templateKey: blog-post
title: Trim unused git branches
today: 2022-05-07
year: 2021
---

## Trim branches no longer on origin

```bash
git remote prune origin --dry-run
git remote prune origin
```

## Find branches already merged

``` bash
git checkout main
# list remote branches that have already been merged into main
git branch -r --merged
# list local branches that have already been merged into main
git branch --merged
```