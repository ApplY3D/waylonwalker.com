---
content: ''
cover: ''
date: 2022-01-07
datetime: 2022-01-07 00:00:00+00:00
description: ''
long_description: ''
now: 2022-05-07 21:32:25.892881
path: pages/blog/pipx-examples.md
slug: pipx-examples
status: draft
super_description: ''
tags:
- python
- linux
- cli
templateKey: blog-post
title: pipx examples
today: 2022-05-07
year: 2022
---

## count lines of code

``` bash
pipx run pygount markata
pipx run pygount markata --format=summary
pipx run pygount markata --suffix=cfg,py,yml
```