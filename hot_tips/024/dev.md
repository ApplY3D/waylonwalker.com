---
canonical_url: https://waylonwalker.com/hot_tips/024/
cover_image: https://images.waylonwalker.com/hot_tips/024.png
description: Conditionally run GitHub Actions Steps Conditionally run GitHub Actions
  Steps
published: true
tags:
- bash
title: '024'
---

Conditionally run GitHub Actions Steps

``` yaml
- uses: dorny/paths-filter@v2.2.0
  id: filter
  with:
      # inline YAML or path to separate file (e.g.: .github/filters.yaml)
      filters: |
      backend:
          - 'backend/**/*'
      frontend:
          - 'frontend/**/*'

# run only if 'backend' files were changed
- name: backend unit tests
  if: steps.filter.outputs.backend == 'true'
  run: ...
```