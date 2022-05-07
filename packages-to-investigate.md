---
content: ''
cover: ''
date: 2019-10-14
datetime: 2019-10-14 00:00:00+00:00
description: jmespath jmespath Tabnine Tabnine |-|-| |-|-| I definitely want to try
  this out with kedro. I definitely want to try this out with kedro. Bulwark is a
  package f
long_description: jmespath jmespath Tabnine Tabnine |-|-| |-|-| I definitely want
  to try this out with kedro. I definitely want to try this out with kedro. Bulwark
  is a package for convenient property-based testing of pandas dataframes, supported
  for Python 3.5+. Bulw
now: 2022-05-07 21:32:25.892285
path: pages/notes/packages-to-investigate.md
slug: packages-to-investigate
status: published
super_description: jmespath jmespath Tabnine Tabnine |-|-| |-|-| I definitely want
  to try this out with kedro. I definitely want to try this out with kedro. Bulwark
  is a package for convenient property-based testing of pandas dataframes, supported
  for Python 3.5+. Bulwark is a package for convenient property-based testing of pandas
  dataframes, supported for Python 3.5+.
tags: []
templateKey: blog-post
title: "\U0001F4DD Packages to Investigate Notes"
today: 2022-05-07
year: 2019
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