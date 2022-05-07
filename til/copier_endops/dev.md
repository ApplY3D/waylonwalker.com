---
canonical_url: https://waylonwalker.com/til/copier_endops/
cover_image: https://images.waylonwalker.com/til/copier_endops.png
description: I was completely stuck for awhile.  copier was not replacing my template
  I was completely stuck for awhile.  copier was not replacing my template ! !
published: true
tags:
- python
- bash
title: Changing copier template strings (_endops)
---

I was completely stuck for awhile.  copier was not replacing my template variables.  I found out that adding all these `_endops` fixed it.  Now It will support all of these types of variable wrappers

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