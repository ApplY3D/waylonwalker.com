---
canonical_url: https://waylonwalker.com/fix-crlf-entire-repo/
cover_image: https://images.waylonwalker.com/fix-crlf-entire-repo.png
description: ''
published: true
tags:
- python
title: fix crlf for entire git repo
---

## Final Result

``` bash
git checkout main git reset --hard git rm -rf --cached . echo "* text=auto" > .gitattributes git add .
```