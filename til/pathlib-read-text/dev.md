---
canonical_url: https://waylonwalker.com/til/pathlib-read-text/
cover_image: https://images.waylonwalker.com/til/pathlib-read-text.png
description: When I need to read contents from a plain text file in python I find
  the When I need to read contents from a plain text file in python I find the
published: true
tags:
- python
- python
- python
title: How I read Files in Python
---

When I need to read contents from a plain text file in python I find the easiest way is to just use `Pathlib`.

``` python
from pathlib import Path

Path('path_to_file').read_text()
```