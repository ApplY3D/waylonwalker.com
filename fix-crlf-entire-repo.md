---
content: ''
cover: ''
date: 2021-03-22
datetime: 2021-03-22 00:00:00+00:00
description: ''
long_description: ''
now: 2022-05-07 21:32:25.893260
path: pages/blog/fix-crlf-entire-repo.md
slug: fix-crlf-entire-repo
status: draft
super_description: ''
tags:
- python
templateKey: blog-post
title: fix crlf for entire git repo
today: 2022-05-07
year: 2021
---

## Final Result

``` bash
git checkout main
git reset --hard
git rm -rf --cached .
echo "* text=auto" > .gitattributes
git add .
```