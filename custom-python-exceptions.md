---
content: ''
cover: ''
date: 2019-09-25
datetime: 2019-09-25 00:00:00+00:00
description: Custom Python Exceptions
long_description: ''
now: 2022-05-07 21:32:25.892292
path: pages/notes/custom-python-exceptions.md
slug: custom-python-exceptions
status: published
super_description: ''
tags: []
templateKey: blog-post
title: Custom Python Exceptions
today: 2022-05-07
year: 2019
---

## Custom Exceptions

```
class ProjectNameError(NameError):
    pass


class UserNameError(NameError):
    pass


class CondaEnvironmentError(RuntimeError):
    pass


class BucketNotDefinedError(NameError):
    pass

```