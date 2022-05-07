---
canonical_url: https://waylonwalker.com/trim-branches/
cover_image: https://images.waylonwalker.com/trim-branches.png
description: ''
published: true
tags:
- git
- bash
- linux
title: Trim unused git branches
---

## Trim branches no longer on origin

```bash
git remote prune origin --dry-run git remote prune origin
```

## Find branches already merged

``` bash
git checkout main
# list remote branches that have already been merged into main
git branch -r --merged
# list local branches that have already been merged into main
git branch --merged
```