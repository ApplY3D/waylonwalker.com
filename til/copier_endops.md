---
content: ''
cover: ''
date: 2022-01-04
datetime: 2022-01-04 00:00:00+00:00
description: I was completely stuck for awhile.  copier was not replacing my template
  I was completely stuck for awhile.  copier was not replacing my template ! !
long_description: I was completely stuck for awhile.  copier was not replacing my
  template I was completely stuck for awhile.  copier was not replacing my template
  ! !
now: 2022-05-07 21:32:25.891831
path: pages/til/copier_endops.md
slug: til/copier_endops
status: published
super_description: I was completely stuck for awhile.  copier was not replacing my
  template I was completely stuck for awhile.  copier was not replacing my template
  ! !
tags:
- python
- bash
templateKey: til
title: Changing copier template strings (_endops)
today: 2022-05-07
year: 2022
---

I was completely stuck for awhile.  copier was not replacing my template
variables.  I found out that adding all these `_endops` fixed it.  Now
It will support all of these types of variable wrappers

``` yaml
# copier.yml
_templates_suffix: .jinja
_envops:
  block_end_string: "%}"
  block_start_string: "{%"
  comment_end_string: "#}"
  comment_start_string: "{#"
  keep_trailing_newline: true
  variable_end_string: "}}"
  variable_start_string: "{{"
```

> !RTFM: Later I read the docs and realized that copier defaults to using `[[`
> and `]]` for its templates unlike other tools like cookiecutter.