---
canonical_url: https://waylonwalker.com/hot_tips/019/
cover_image: https://images.waylonwalker.com/hot_tips/019.png
description: ''
published: true
tags:
- bash
title: 019
---

## batch rename files
## with **bash**

``` bash
for f in *.jpeg; do
    mv -- "$f" "${f%.jpeg}.jpg"
done
```