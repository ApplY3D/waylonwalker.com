---
canonical_url: https://waylonwalker.com/hot_tips/011/
cover_image: https://images.waylonwalker.com/hot_tips/011.png
description: 'Load  Load '
published: true
tags:
- data
- python
title: '011'
---

Load _data_ from database into **pandas**

``` python
import pandas as pd from sqlalchemy import create engine

engine = create_engine('postgresql://scott:tiger@localhost:5432/mydatabase')

sql = 'select * from inventory'

with engine.connect() as connection:
    inventory = pd.read_sql(sql, con)
engine.dispose()

```