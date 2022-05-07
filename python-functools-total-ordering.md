---
content: ''
cover: ''
date: 2022-01-14
datetime: 2022-01-14 00:00:00+00:00
description: 'functools.total functools.total From the Docs: The class must define
  one of  From the Docs: The class must define one of  Here is an example using the
  Enum I wa'
long_description: 'functools.total functools.total From the Docs: The class must define
  one of  From the Docs: The class must define one of  Here is an example using the
  Enum I was working on the other day. Here is an example using the Enum I was working
  on the other d'
now: 2022-05-07 21:32:25.894532
path: pages/blog/python-functools-total-ordering.md
slug: python-functools-total-ordering
status: published
super_description: 'functools.total functools.total From the Docs: The class must
  define one of  From the Docs: The class must define one of  Here is an example using
  the Enum I was working on the other day. Here is an example using the Enum I was
  working on the other day.'
tags:
- python
templateKey: til
title: python functools total ordering
today: 2022-05-07
year: 2022
---

functools.total_ordering makes adding all of six of the rich comparison
operators to your custom classes much easier, and more likely that you
remember all of them.

> From the Docs: The class must define one of \_\_lt\_\_(), \_\_le\_\_(),
> \_\_gt\_\_(), or \_\_ge\_\_ In addition, the class should supply an
> \_\_eq\_\_() method.

[Total Ordering Docs](https://docs.python.org/3/library/functools.html#functools.total_ordering)

Here is an example using the Enum I was working on the other day.

``` python
from enum import Enum, auto
from functools import total_ordering


@total_ordering
class LifeCycle(Enum):

    configure = auto()
    glob = auto()
    load = auto()
    pre_render = auto()
    render = auto()
    post_render = auto()
    save = auto()

    def __lt__(self, other):
        try:
            return self.value < other.value
        except AttributeError:
            return self.value < other

    def __eq__(self, other):
        try:
            return self.value == other.value
        except AttributeError:
            return self.value == other

```