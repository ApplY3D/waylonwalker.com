---
canonical_url: https://waylonwalker.com/last-n-git-files/
cover_image: https://images.waylonwalker.com/last-n-git-files.png
description: ''
published: true
tags: []
title: List the latest files to change in a git repo
---

``` bash
while read file; do echo $(git log --pretty=format:%ad -n 1 --date=raw -- $file) $file; done < <(git ls-tree -r --name-only HEAD | grep static/stories) | sort -r | head -n 3 | cut -d " " -f 3
```