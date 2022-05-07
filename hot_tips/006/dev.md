---
canonical_url: https://waylonwalker.com/hot_tips/006/
cover_image: https://images.waylonwalker.com/hot_tips/006.png
description: 'Setup  Setup '
published: true
tags:
- git
- python
- cli
title: '006'
---

Setup **pre-commit** for _isort_

``` yaml
  - repo: https://github.com/asottile/seed-isort-config
    rev: v2.1.1
    hooks:
      - id: seed-isort-config
  - repo: https://github.com/pre-commit/mirrors-isort
    rev: v4.3.21
    hooks:
      - id: isort
```

_includes automatic_ .isort-config