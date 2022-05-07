---
canonical_url: https://waylonwalker.com/hot_tips/012/
cover_image: https://images.waylonwalker.com/hot_tips/012.png
description: "\U0001F446 add this to your  \U0001F446 add this to your "
published: true
tags:
- python
title: '012'
---

**autoreload** your imports in ipython for ⚡ fast development

``` python
c.InteractiveShellApp.extensions = ['autoreload'] c.InteractiveShellApp.exec_lines = ['%autoreload 2'] c.InteractiveShellApp.exec_lines.append('print("Warning: disable autoreload in ipython_config.py to improve performance.")')
```
👆 add this to your `~/.ipython/profile_default/ipython_config.py.`