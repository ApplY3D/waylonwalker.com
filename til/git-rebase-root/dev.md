---
canonical_url: https://waylonwalker.com/til/git-rebase-root/
cover_image: https://images.waylonwalker.com/til/git-rebase-root.png
description: Git has a built in way to rebase all the way back to the beginning of
  Git has a built in way to rebase all the way back to the beginning of
published: true
tags:
- git
- cli
title: Git rebase to the beginning of time
---

Git has a built in way to rebase all the way back to the beginning of time.  There is no need to scroll through the log to find the first hash, or find the total number of commits. Just use `--root`.

``` bash
git rebase --root
```