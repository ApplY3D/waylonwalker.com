---
canonical_url: https://waylonwalker.com/hot_tips/018/
cover_image: https://images.waylonwalker.com/hot_tips/018.png
description: ''
published: true
tags:
- python
title: 018
---

## Sending `**kwargs`

``` python
def func(**kwargs):
    print(kwargs) # kwargs are a dictionary!

>>> func(**{'one':'a', 'two':'b')
{'one': 'a', 'two': 'b'}
```