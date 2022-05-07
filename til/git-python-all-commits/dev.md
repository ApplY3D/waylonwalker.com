---
canonical_url: https://waylonwalker.com/til/git-python-all-commits/
cover_image: https://images.waylonwalker.com/til/git-python-all-commits.png
description: ''
published: true
tags:
- python
title: List all git commits with GitPython
---

``` python
from git import Repo

repo = Repo('.') commits = repo.iter_commits()
```