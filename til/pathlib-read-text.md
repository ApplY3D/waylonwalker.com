---
content: ''
cover: ''
date: 2022-03-20
datetime: 2022-03-20 00:00:00+00:00
description: When I need to read contents from a plain text file in python I find
  the When I need to read contents from a plain text file in python I find the
long_description: When I need to read contents from a plain text file in python I
  find the When I need to read contents from a plain text file in python I find the
now: 2022-05-07 21:32:25.891852
path: pages/til/pathlib-read-text.md
slug: til/pathlib-read-text
status: published
super_description: When I need to read contents from a plain text file in python I
  find the When I need to read contents from a plain text file in python I find the
tags:
- python
- python
- python
templateKey: til
title: How I read Files in Python
today: 2022-05-07
year: 2022
---

When I need to read contents from a plain text file in python I find the
easiest way is to just use `Pathlib`.

``` python
from pathlib import Path

Path('path_to_file').read_text()
```