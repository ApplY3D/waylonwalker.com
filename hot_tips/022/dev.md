---
canonical_url: https://waylonwalker.com/hot_tips/022/
cover_image: https://images.waylonwalker.com/hot_tips/022.png
description: Move files then symlink them
published: true
tags:
- bash
title: '022'
---

## File System Full 🤔

_Move files then symlink them_

## with **Bash**

``` bash
mkdir /mnt/mounted_drive mv ~/bigdir /mnt/mounted_drive ln -s /mnt/mounted_drive/bigdir ~/bigdir
```