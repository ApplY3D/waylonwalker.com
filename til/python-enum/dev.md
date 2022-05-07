---
canonical_url: https://waylonwalker.com/til/python-enum/
cover_image: https://images.waylonwalker.com/til/python-enum.png
description: 'Python comes with an enum module for creating enums.  You can make your
  Python comes with an enum module for creating enums.  You can make your Enum values
  can '
published: true
tags:
- python
- python
- python
title: Python Enum
---

Python comes with an enum module for creating enums.  You can make your own enum by inheriting importing and inheriting from Enum.

```
from enum import Enum


class LifeCycle(Enum):
    configure = 1
    glob = 2
    pre_render = 3
    render = 4
    post_render = 5
    save = 6
```

## auto incrementing

Enum values can be auto incremented by importing auto, and calling
`auto()` as their value.

``` python
from enum import Enum, auto


class LifeCycle(Enum):
    configure = auto()
    glob = auto()
    pre_render = auto()
    render = auto()
    post_render = auto()
    save = auto()
```

## using the enum

Enum's are accessed directy under the class itself, and have primarily two methods underneath each thing you make, `.name` and `.value`.

``` python
Lifecycle.glob Lifecycle.glob.value Lifecycle.glob.name
```

![using the Lifecycle Enum](https://images.waylonwalker.com/using-lifecycle-enum.png)