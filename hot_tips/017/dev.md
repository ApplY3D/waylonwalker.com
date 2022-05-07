---
canonical_url: https://waylonwalker.com/hot_tips/017/
cover_image: https://images.waylonwalker.com/hot_tips/017.png
description: order matters
published: true
tags:
- python
title: '017'
---

## Sending `*args`

``` python
def func(one, two):
    print(f'two is {two}')


>>> func(*['a', 'b'])
two is b
```

**order matters**