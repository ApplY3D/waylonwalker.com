---
content: ''
cover: ''
date: 2022-03-31
datetime: 2022-03-31 00:00:00+00:00
description: I ran into a PR this week where the author was inheriting what BaseException
  I ran into a PR this week where the author was inheriting what BaseException Try
  ru
long_description: I ran into a PR this week where the author was inheriting what BaseException
  I ran into a PR this week where the author was inheriting what BaseException Try
  running these examples in a  Try running these examples in a  Since things such
  as  Since th
now: 2022-05-07 21:32:25.891484
path: pages/til/python-base-exception.md
slug: til/python-base-exception
status: published
super_description: I ran into a PR this week where the author was inheriting what
  BaseException I ran into a PR this week where the author was inheriting what BaseException
  Try running these examples in a  Try running these examples in a  Since things such
  as  Since things such as  If you except from exception or something than inherits
  from it you will be If you except from exception or something than inherits from
  it you will be When you make custom exceptions expect that users, or your team members
  will When yo
tags:
- python
templateKey: til
title: Don't inherit from python BaseException, Here's why.
today: 2022-05-07
year: 2022
---

I ran into a PR this week where the author was inheriting what BaseException
rather than exception.  I made this example to illustrate the unintended side
effects that it can have.

Try running these examples in a `.py` file for yourself and try to kill them
with control-c.

## You cannot Keybard interrupt

Since things such as `KeyboardInterrupt` are created as an exception that
inherits from `BaseException`, if you except `BaseException` you can no longer
`KeyboardInterrupt`.

```python
from time import sleep

while True:
    try:
        sleep(30)
    except BaseException: # ❌
        pass
```

## except from Exception or higher

If you except from exception or something than inherits from it you will be
better off, and avoid unintended side effects.

```python
from time import sleep

while True:
    try:
        sleep(30)
    except Exception: # ✅
        pass
```

## This goes with Custom Exceptions as well

When you make custom exceptions expect that users, or your team members will
want to catch them and try to handle them if they can.  If you inherit from
`BaseException` you will put them in a similar situation when they use your
custom Exception.

```python
class MyFancyException(BaseException): # ❌
    ...

class MyFancyException(Exception): # ✅
    ...
```