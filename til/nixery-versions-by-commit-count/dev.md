---
canonical_url: https://waylonwalker.com/til/nixery-versions-by-commit-count/
cover_image: https://images.waylonwalker.com/til/nixery-versions-by-commit-count.png
description: I was listening to  I was listening to  Since many things still want
  to see a version number, there is one automatic Since many things still want to
  see a versi
published: true
tags:
- catalytic
title: Nix Versions By Commit Count
---

I was listening to [shipit37](https://changelog.com/shipit/37) with Vincent Ambo talking about building fully declaritive systems with nix.  Vincent is building out Nixery and strongly believes that standard versioning systems are flawed.  If we have good ci setup, and every commit is a good commit the idea of a release is just some arbitrary point in history that the maintainer decided was a good time to release, and has less to do about features and quality.

Since many things still want to see a version number, there is one automatic always increasing number that is a part of every single git repo, and that is the commit count.  Nixery is versioned by commit count.  When counting on the main branch there is no way for two points in time to share the same version. The git cli will count all commits by default so you have to be careful to only include commits from the branch you want to version/release from.

``` bash
git rev-list main --count
```