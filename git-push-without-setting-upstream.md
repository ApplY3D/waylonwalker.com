---
content: ''
cover: ''
date: 2020-02-04
datetime: 2020-02-04 00:00:00+00:00
description: 'Finally after years of hand typing out a full  Finally after years of
  hand typing out a full  This one setting will now  This one setting will now '
long_description: 'Finally after years of hand typing out a full  Finally after years
  of hand typing out a full  This one setting will now  This one setting will now '
now: 2022-05-07 21:32:25.893917
path: pages/blog/git-push-without-setting-upstream.md
slug: git-push-without-setting-upstream
status: published
super_description: 'Finally after years of hand typing out a full  Finally after years
  of hand typing out a full  This one setting will now  This one setting will now '
tags:
- git
- cli
templateKey: blog-post
title: git push without setting upstream
today: 2022-05-07
year: 2020
---

Finally after years of hand typing out a full `git push --upstream
my_really_long_and_descriptive_branch_name` I found there is a setting to
automatcally push to the current branch. More realisitically I just did a `git
push` let git yell at me, and copying the suggestion.

## git config

``` bash
git config --global push.default current
```

This one setting will now `git push` to the current branch without yelling at
you that your upstream does not match your current branch.  This helps me ship
chnages faster as I am constantly chnaging projects and branches.