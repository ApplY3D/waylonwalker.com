---
content: ''
cover: ''
date: 2020-10-08
datetime: 2020-10-08 00:00:00+00:00
description: ''
long_description: ''
now: 2022-05-07 21:32:25.893743
path: pages/blog/last-n-git-files.md
slug: last-n-git-files
status: 'false'
super_description: ''
tags: []
templateKey: blog-post
title: List the latest files to change in a git repo
today: 2022-05-07
year: 2020
---

``` bash
while read file; do echo $(git log --pretty=format:%ad -n 1 --date=raw -- $file) $file; done < <(git ls-tree -r --name-only HEAD | grep static/stories) | sort -r | head -n 3 | cut -d " " -f 3
```