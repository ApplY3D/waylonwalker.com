---
canonical_url: https://waylonwalker.com/find-replace/
cover_image: https://images.waylonwalker.com/find-replace.png
description: notes about find and replace techniques
published: true
tags:
- linux
- bash
title: Find and Replace in the Terminal.
---

## grepr

```bash
grepr() {grep -iRl "$1" | xargs sed -i "s/$1/$2/g"}

```bash
grepr() {grep -iRl "$1" | xargs sed -i "s/$1/$2/g"}
```

## grepd

``` python
grepd() {grep -iRl "$1" | xargs sed -i "/^$1/d"}
```

## CocSearch


``` bash
:CocSearch status: 'false' -g *.md
```