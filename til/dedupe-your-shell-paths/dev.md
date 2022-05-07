---
canonical_url: https://waylonwalker.com/til/dedupe-your-shell-paths/
cover_image: https://images.waylonwalker.com/til/dedupe-your-shell-paths.png
description: 'If you have ever ran  If you have ever ran '
published: true
tags:
- linux
- cli
title: Dedupe your shell paths
---

If you have ever ran `which <command>` and see duplicate entries it's likely that you have duplicate entries in your $PATH.  You can clean this up with a one liner at the end of your bashrc or zshrc.

``` bash
eval "typeset -U path"
```