---
canonical_url: https://waylonwalker.com/packages-to-investigate/
cover_image: https://images.waylonwalker.com/packages-to-investigate.png
description: jmespath jmespath Tabnine Tabnine |-|-| |-|-| I definitely want to try
  this out with kedro. I definitely want to try this out with kedro. Bulwark is a
  package f
published: true
tags: []
title: "\U0001F4DD Packages to Investigate Notes"
---

* jmespath
* Tabnine

## Bulwark

|-|-|
|github: |[https://github.com/zaxr/bulwark](https://github.com/zaxr/bulwark)|

I definitely want to try this out with kedro.

Bulwark is a package for convenient property-based testing of pandas dataframes, supported for Python 3.5+.

## Example

        import bulwark.decorators as dc

        @dc.IsShape((-1, 10))
        @dc.IsMonotonic(strict=True)
        @dc.HasNoNans()
        def compute(df):
            # complex operations to determine result
            ...
        return result_df