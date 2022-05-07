---
canonical_url: https://waylonwalker.com/update-copier/
cover_image: https://images.waylonwalker.com/update-copier.png
description: 'Copier is a fantastic templating library written in python, but older
  versions Copier is a fantastic templating library written in python, but older versions
  I '
published: true
tags:
- python
- python
- python
title: Copier < 6.0.0b0 considered dangerous
---

Copier is a fantastic templating library written in python, but older versions have a dangerous bug if you are using it inside of existing directories.

## This is a PSA

I Use copier several times per day and get fantastic benefit from this project, this post is not intended to crap all over copier in any way, but is rather a PSA for other users who do use copier like I do so that they know the dangers of using copier inside an existing directory.

## The issue

## The fix

https://github.com/copier-org/copier/pull/273

As of the time of writing this version is still in beta, if you still want to use copier with existing directtories, I'd strongly encourage you to install the `--pre` release.

``` python
pipx install copier --pip-args='--pre'
```

## confirm

``` bash
copier --version
# copier 6.0.0b0
```


## My update commit

https://github.com/WaylonWalker/devtainer/commit/a06e47462e2c6d26ad69fbdc2e7990a1a73ab4b7