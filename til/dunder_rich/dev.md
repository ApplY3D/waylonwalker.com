---
canonical_url: https://waylonwalker.com/til/dunder_rich/
cover_image: https://images.waylonwalker.com/til/dunder_rich.png
description: 'Adding a  Adding a '
published: true
tags:
- python
- rich
title: Adding __rich__ methods to python classes
---

Adding a `__render__` method that returns a rich renderable to any python class makes it display this output if printed with rich.  This also includes being nested inside a rich Layout.


``` python
import rich from rich.panel import Panel


class ShowMe:
    def __rich__(self):
        return Panel("hello", border_style="gold1")


if __name__ == "__main__":
    rich.print(ShowMe())
```

![results of printing ShowMe with rich](https://images.waylonwalker.com/dunder_rich_showme.png)