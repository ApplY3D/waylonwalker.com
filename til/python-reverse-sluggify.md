---
content: ''
cover: ''
date: 2022-01-20
datetime: 2022-01-20 00:00:00+00:00
description: 'In order to make an auto title plugin for markata I needed to come up
  In order to make an auto title plugin for markata I needed to come up ! ! Here I
  have  a  '
long_description: In order to make an auto title plugin for markata I needed to come
  up In order to make an auto title plugin for markata I needed to come up ! ! Here
  I have  a  Here I have  a  To turn this into a markata plugin I put it into a pre
  To turn this into a
now: 2022-05-07 21:32:25.891793
path: pages/til/python-reverse-sluggify.md
slug: til/python-reverse-sluggify
status: published
super_description: In order to make an auto title plugin for markata I needed to come
  up In order to make an auto title plugin for markata I needed to come up ! ! Here
  I have  a  Here I have  a  To turn this into a markata plugin I put it into a pre
  To turn this into a markata plugin I put it into a pre
tags:
- python
templateKey: til
title: Python Reverse Sluggify
today: 2022-05-07
year: 2022
---

In order to make an auto title plugin for markata I needed to come up
with a way to reverse the slug of a post to create a title for one that
does not explicitly have a title.

!!! Note "slugs"
   a slug is generally all lowercase and free of spaces, and is a way to
   make website routes (urls)


Here I have  a `path` available that gives me the articles path, ex.
`python-reverse-sluggify.md`.  An easy way to get rid of the file
extension, is to pass it into pathlib.Path and ask for the stem, which
returns `python-reverse-sluggify`.  Then from There I chose to replace
`-` and `_` with a space.

``` python
article["title"] = (
    Path(article["path"]).stem.replace("-", " ").replace("_", " ").title()
)
```



To turn this into a markata plugin I put it into a pre_render hook.

``` python
from pathlib import Path

from markata.hookspec import hook_impl, register_attr


@hook_impl
@register_attr("articles")
def pre_render(markata) -> None:
    for article in markata.filter('title==""'):
        article["title"] = (
            Path(article["path"]).stem.replace("-", " ").replace("_", " ").title()
        )
```