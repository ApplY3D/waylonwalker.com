---
content: ''
cover: ''
date: 2022-05-07
datetime: 2022-05-07 00:00:00+00:00
description: ''
long_description: ''
now: 2022-05-07 21:32:25.891312
path: pages/til/git-python-all-commits.md
slug: til/git-python-all-commits
status: published
super_description: ''
tags:
- python
templateKey: til
title: List all git commits with GitPython
today: 2022-05-07
year: 2022
---

``` python
from git import Repo

repo = Repo('.')
commits = repo.iter_commits()
```