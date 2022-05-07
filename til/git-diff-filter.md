---
content: ''
cover: ''
date: 2022-02-27
datetime: 2022-02-27 00:00:00+00:00
description: Git commands such as  Git commands such as  You can find the full description
  by searching for  You can find the full description by searching for  Open up a
  gi
long_description: Git commands such as  Git commands such as  You can find the full
  description by searching for  You can find the full description by searching for  Open
  up a git repo and play around with this, here are some example that Open up a git
  repo and play a
now: 2022-05-07 21:32:25.891370
path: pages/til/git-diff-filter.md
slug: til/git-diff-filter
status: published
super_description: Git commands such as  Git commands such as  You can find the full
  description by searching for  You can find the full description by searching for  Open
  up a git repo and play around with this, here are some example that Open up a git
  repo and play around with this, here are some example that
tags:
- git
templateKey: til
title: git diff-filter
today: 2022-05-07
year: 2022
---

Git commands such as `diff`, `log`, `whatchanged` all take a flag called
`--diff-filter`.  This can filter for only certain types of diffs, such
as added (A), modified (M), or deleted (D).

## Man page

You can find the full description by searching for `--diff-filter` in
the `man git diff` page.

``` bash
--diff-filter=[(A|C|D|M|R|T|U|X|B)...[*]]
    Select only files that are Added (A), Copied (C), Deleted (D), Modified (M), Renamed (R), have their type (i.e. regular file, symlink, submodule, ...)
    changed (T), are Unmerged (U), are Unknown (X), or have had their pairing Broken (B). Any combination of the filter characters (including none) can be used.
    When * (All-or-none) is added to the combination, all paths are selected if there is any file that matches other criteria in the comparison; if there is no
    file that matches other criteria, nothing is selected.

    Also, these upper-case letters can be downcased to exclude. E.g.  --diff-filter=ad excludes added and deleted paths.

    Note that not all diffs can feature all types. For instance, diffs from the index to the working tree can never have Added entries (because the set of paths
    included in the diff is limited by what is in the index). Similarly, copied and renamed entries cannot appear if detection for those types is disabled.
```

## Try it out

Open up a git repo and play around with this, here are some example that
I played with that seemed useful to me.

``` bash
# find when any files were deleted
git log --diff-filter D

# find when all files were added
git log --diff-filter A

# only one specific file
git log --diff-filter A -- readme.md

# partial match to a single file
git log --diff-filter A -- read*

# Find when all python files were added
git log --diff-filter A -- *.py
```