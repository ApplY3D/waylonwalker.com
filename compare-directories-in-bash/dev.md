---
canonical_url: https://waylonwalker.com/compare-directories-in-bash/
cover_image: https://images.waylonwalker.com/compare-directories-in-bash.png
description: Today I needed to check for articles that used the same slug from two
  directories, bash made it super simple. Today I needed to check for articles that
  used the
published: true
tags:
- bash
- tip
title: Compare Directories In Bash
---

Today I needed to check for articles that used the same slug from two directories, bash made it super simple.

``` bash
diff -rq src/pages/blog src/pages/notes
```