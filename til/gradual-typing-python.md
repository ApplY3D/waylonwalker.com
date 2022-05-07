---
content: ''
cover: ''
date: 2022-01-21
datetime: 2022-01-21 00:00:00+00:00
description: I I https://youtu.be/Rk-Y71P https://youtu.be/Rk-Y71P Run Mypy as is,
  don Run Mypy as is, don Next we will add  Next we will add  The final stage to this
  series
long_description: I I https://youtu.be/Rk-Y71P https://youtu.be/Rk-Y71P Run Mypy as
  is, don Run Mypy as is, don Next we will add  Next we will add  The final stage
  to this series is to add  The final stage to this series is to add  Make sure that
  you watch Anthony Mak
now: 2022-05-07 21:32:25.891746
path: pages/til/gradual-typing-python.md
slug: til/gradual-typing-python
status: published
super_description: I I https://youtu.be/Rk-Y71P https://youtu.be/Rk-Y71P Run Mypy
  as is, don Run Mypy as is, don Next we will add  Next we will add  The final stage
  to this series is to add  The final stage to this series is to add  Make sure that
  you watch Anthony Make sure that you watch Anthony https://www.youtube.com/watch?v=Rk-Y71P
  https://www.youtube.com/watch?v=Rk-Y71P
tags:
- python
templateKey: til
title: Gradual Typing in Python
today: 2022-05-07
year: 2022
---

I've referenced a video from Anthony Sotile in passing conversation several
times.  Walking through his gradual typing process has really helped me
understand typing better, and has helped me make some projects better over time
rather than getting slammed with typing errors.

https://youtu.be/Rk-Y71P_9KE

# Step 1

Run Mypy as is, don't get fancy yet.  This will not reach into any functions
unless they are alreay explicitly typed.  It will not enforce you to type them
either.

``` bash
pip install mypy
mypy .
# or your specific project to avoid .venvs
mypy src
# or a single file
mypy my-script.py
```

## Step 2

Next we will add `check-untyped-defs`, this will start checking inside
functions that are not typed.  To add this to your config create a
`setup.cfg` with the following.

``` toml
[mypy]
check_untyped_defs = True
```

## Step 3

The final stage to this series is to add `disallow_untyped_defs`.  This will
start requiring all of your functions to be type hinted.  This one is probably
the toughest, because as you type functions mypy can uncover more issues for
you to fix.  Often times the list of errors grows before it shrinks.

``` toml
[mypy]
check_untyped_defs = True
disallow_untyped_defs = True
```

## Anthony's video

Make sure that you watch Anthony's video, give him a sub, he deserves it
for all the great things he is doing for the python community.

https://www.youtube.com/watch?v=Rk-Y71P_9KE