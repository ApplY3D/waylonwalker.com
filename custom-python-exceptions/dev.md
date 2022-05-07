---
canonical_url: https://waylonwalker.com/custom-python-exceptions/
cover_image: https://images.waylonwalker.com/custom-python-exceptions.png
description: Custom Python Exceptions
published: true
tags: []
title: Custom Python Exceptions
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