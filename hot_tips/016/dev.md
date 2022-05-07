---
canonical_url: https://waylonwalker.com/hot_tips/016/
cover_image: https://images.waylonwalker.com/hot_tips/016.png
description: ''
published: true
tags:
- python
title: '016'
---

## Recieving `**kwargs`

``` python
def funnc(**kwargs):
    print(kwargs) # kwargs are a dictionary!

>>> func(one='a', two='b')
{'one': 'a', 'two': 'b'}
```