---
canonical_url: https://waylonwalker.com/hot_tips/004/
cover_image: https://images.waylonwalker.com/hot_tips/004.png
description: "\U0001F525 #kedrotips use find-kedro to assembly your pipelines \U0001F525
  #kedrotips use find-kedro to assembly your pipelines"
published: true
tags:
- kedro
title: '004'
---

🔥 #kedrotips use find-kedro to assembly your pipelines


``` python
from kedro.context import KedroContext from find_kedro import find_kedro

class ProjectContext(KedroContext):
    def _get_pipelines(self) -> Pipeline:
        return find_kedro()
```