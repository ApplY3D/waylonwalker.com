---
canonical_url: https://waylonwalker.com/hot_tips/009/
cover_image: https://images.waylonwalker.com/hot_tips/009.png
description: 'Combine a directory of  Combine a directory of '
published: true
tags:
- data
- python
title: 009
---

Combine a directory of _csv's_ with **pandas**

``` python
import pandas as pd from pathlib import Path

csvs = Path.glob('raw/*.csv') csvs_combined = pd.concat(csvs) csvs_combined.to_csv('processed/combined.csv')
```