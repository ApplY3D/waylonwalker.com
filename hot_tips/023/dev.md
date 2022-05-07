---
canonical_url: https://waylonwalker.com/hot_tips/023/
cover_image: https://images.waylonwalker.com/hot_tips/023.png
description: Find and replace Groups in VSCode Find and replace Groups in VSCode
published: true
tags:
- bash
title: '023'
---

Find and replace Groups in VSCode
$1 referrs to the second group

```
(filepath: top)(.*)
filepath: s3://bucket/top$1.parquet
```

``` diff
- filepath: top/raw/scooters
+ filepath: s3://bucket/top/raw/scooters.parquet
```