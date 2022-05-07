---
content: ''
cover: ''
date: 2022-02-02
datetime: 2022-02-02 00:00:00+00:00
description: I was listening to  I was listening to  Since many things still want
  to see a version number, there is one automatic Since many things still want to
  see a versi
long_description: I was listening to  I was listening to  Since many things still
  want to see a version number, there is one automatic Since many things still want
  to see a version number, there is one automatic
now: 2022-05-07 21:32:25.891398
path: pages/til/nixery-versions-by-commit-count.md
slug: til/nixery-versions-by-commit-count
status: published
super_description: I was listening to  I was listening to  Since many things still
  want to see a version number, there is one automatic Since many things still want
  to see a version number, there is one automatic
tags:
- catalytic
templateKey: til
title: Nix Versions By Commit Count
today: 2022-05-07
year: 2022
---

I was listening to [shipit37](https://changelog.com/shipit/37) with Vincent
Ambo talking about building fully declaritive systems with nix.  Vincent is
building out Nixery and strongly believes that standard versioning systems are
flawed.  If we have good ci setup, and every commit is a good commit the idea
of a release is just some arbitrary point in history that the maintainer
decided was a good time to release, and has less to do about features and
quality.

Since many things still want to see a version number, there is one automatic
always increasing number that is a part of every single git repo, and that is
the commit count.  Nixery is versioned by commit count.  When counting on the
main branch there is no way for two points in time to share the same version.
The git cli will count all commits by default so you have to be careful to only
include commits from the branch you want to version/release from.

``` bash
git rev-list main --count
```