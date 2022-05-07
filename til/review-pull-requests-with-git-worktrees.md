---
content: ''
cover: ''
date: 2022-05-04
datetime: 2022-05-04 00:00:00+00:00
description: 'Sometimes you get a PR on a project, but cannot review it without wrecking
  your Sometimes you get a PR on a project, but cannot review it without wrecking
  your '
long_description: 'Sometimes you get a PR on a project, but cannot review it without
  wrecking your Sometimes you get a PR on a project, but cannot review it without
  wrecking your This will create a new directory  This will create a new directory '
now: 2022-05-07 21:32:25.892039
path: pages/til/review-pull-requests-with-git-worktrees.md
slug: til/review-pull-requests-with-git-worktrees
status: published
super_description: 'Sometimes you get a PR on a project, but cannot review it without
  wrecking your Sometimes you get a PR on a project, but cannot review it without
  wrecking your This will create a new directory  This will create a new directory '
tags:
- git
templateKey: til
title: Review Pull Requests with git worktrees
today: 2022-05-07
year: 2022
---

Sometimes you get a PR on a project, but cannot review it without wrecking your
current working setup.  This might be because it needs to be compiled, or a new
set of requirements.  Git worktrees is a great way to chekout the remote branch
in a completely separate directory to avoid changing any files in your current
project.

``` bash
# pattern
# git worktree add -b <branch-name> <PATH> <remote>/<branch-name>
git worktree add -b fix-aws-service-cnsn /tmp/project origin/fix-aws-service-cnsn
```

This will create a new directory `/tmp/project` that you can review the branch
`fix-aws-service-cnsn` from the remote `origin`.  If you have setup different remotes locally you can check for the name of it with `git remote -v`