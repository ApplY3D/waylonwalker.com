---
content: ''
cover: ''
date: 2022-02-28
datetime: 2022-02-28 00:00:00+00:00
description: Listing all the deleted files in all of git history can be done by Listing
  all the deleted files in all of git history can be done by These various commands
  wil
long_description: Listing all the deleted files in all of git history can be done
  by Listing all the deleted files in all of git history can be done by These various
  commands will show all files that were ever deleted on These various commands will
  show all files that
now: 2022-05-07 21:32:25.891384
path: pages/til/git-find-deleted-files.md
slug: til/git-find-deleted-files
status: published
super_description: Listing all the deleted files in all of git history can be done
  by Listing all the deleted files in all of git history can be done by These various
  commands will show all files that were ever deleted on These various commands will
  show all files that were ever deleted on The reflog can be super powerful in finding
  lost files here, as it only The reflog can be super powerful in finding lost files
  here, as it only
tags:
- git
templateKey: til
title: git find deleted files
today: 2022-05-07
year: 2022
---

Listing all the deleted files in all of git history can be done by
combining `git log` with `--diff-filter`.  The log gives you lots of
options to show different bits of information about the commit that
happened at that point.  It's even possible to get a completely clean
list of files that are in your git history but have been deleted.

## git log --diff-filter

These various commands will show all files that were ever deleted on
your current branch.

``` bash
# This one includes the date, commit hash, and Author
git log --diff-filter D

# this one could be a git alias, but includes empty lines
git log --diff-filter D --pretty="format:" --name-only

# this one has the empty lines cleaned up
git log --diff-filter D --pretty="format:" --name-only | sed '/^$/d'
```
## git reflog --diff-filter

The reflog can be super powerful in finding lost files here, as it only
cares about git operations, not just the current branch.  It will search
accross all branches for deleted files and report them.

``` bash
# This one includes the commit hash, branch, tag, and commit message
git reflog --diff-filter D

# You might want to at least add the filename
git reflog --diff-filter D --name-only

# this one could be a git alias, but includes empty lines
git reflog --diff-filter D --pretty="format:" --name-only

# this one has the empty lines cleaned up
git reflog --diff-filter D --pretty="format:" --name-only | sed '/^$/d'
```