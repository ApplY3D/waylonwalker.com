---
content: ''
cover: ''
date: 2019-01-21
datetime: 2019-01-21 00:00:00+00:00
description: https://blog.ostermiller.org/removing-and-purging-files-from-git-history/
  https://blog.ostermiller.org/removing-and-purging-files-from-git-history/
long_description: https://blog.ostermiller.org/removing-and-purging-files-from-git-history/
  https://blog.ostermiller.org/removing-and-purging-files-from-git-history/
now: 2022-05-07 21:32:25.892643
path: pages/blog/git-rm-cruft.md
slug: git-rm-cruft
status: draft
super_description: https://blog.ostermiller.org/removing-and-purging-files-from-git-history/
  https://blog.ostermiller.org/removing-and-purging-files-from-git-history/
tags:
- git
templateKey: blog-post
title: remove git cruft
today: 2022-05-07
year: 2019
---

## inspiration

https://blog.ostermiller.org/removing-and-purging-files-from-git-history/

``` bash
git log --all --pretty=format: --name-only --diff-filter=D | sed -r 's|[^/]+$||g' | sort -u
```
``` bash
git filter-branch --tag-name-filter cat --index-filter 'git rm -r --cached --ignore-unmatch FILE_LIST' --prune-empty -f -- --all
```

``` bash
rm -rf .git/refs/original/
git reflog expire --expire=now --all
git gc --aggressive --prune=now
```

``` bash
git push origin --force --all
git push origin --force --tags
```

``` bash
cd MY_LOCAL_GIT_REPO
git fetch origin
git rebase
git reflog expire --expire=now --all
git gc --aggressive --prune=now
```