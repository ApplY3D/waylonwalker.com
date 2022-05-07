---
content: ''
cover: ''
date: 2022-02-03
datetime: 2022-02-03 00:00:00+00:00
description: For an embarassingly long time, til today, I have been wrapping my dict
  For an embarassingly long time, til today, I have been wrapping my dict Lets consider
  th
long_description: For an embarassingly long time, til today, I have been wrapping
  my dict For an embarassingly long time, til today, I have been wrapping my dict
  Lets consider this example for prices of supplies.  Here we set a variable of Lets
  consider this example f
now: 2022-05-07 21:32:25.891523
path: pages/til/python-dict-get.md
slug: til/python-dict-get
status: published
super_description: For an embarassingly long time, til today, I have been wrapping
  my dict For an embarassingly long time, til today, I have been wrapping my dict
  Lets consider this example for prices of supplies.  Here we set a variable of Lets
  consider this example for prices of supplies.  Here we set a variable of What I
  would always do is try to get the key, and if it failed on KeyError, I What I would
  always do is try to get the key, and if it failed on KeyError, I What I noticed
  Nic does is to use get.  This
tags:
- python
templateKey: til
title: python dict get
today: 2022-05-07
year: 2022
---

For an embarassingly long time, til today, I have been wrapping my dict
gets with key errors in python.  I'm sure I've read it in code a bunch
of times, but just brushed over why you would use get.  That is until I
read a bunch of PR's from my buddy Nic and notice that he never gets
things with brackets and always with `.get`.  This turns out so much
cleaner to create a default case than try except.


## Example

Lets consider this example for prices of supplies.  Here we set a variable of
prices as a dictionary of items and thier price.

```python
prices = {'pen': 1.2, 'pencil', 0.3, 'eraser', 2.3}
```

## Except KeyError

What I would always do is try to get the key, and if it failed on KeyError, I
would set the value (`paper_price` in this case) to a default value.

```python
try:
    paper_price = prices['paper']
except KeyError:
    paper_price = None
```

## .get

What I noticed Nic does is to use get.  This feels just so much cleaner that
it's a one liner and feels much easier to read and understand that if there is
no price for paper we set it to `None`.

```python
paper_price = prices.get('paper', None)
```

We can just as easily set the default to other values.  Let's consider sales
for instance.  If there is not a record for the sale of paper, it might be that
we sold 0 paper in the given dataset.

```python
paper_sales = sales.get('paper', 0)
```