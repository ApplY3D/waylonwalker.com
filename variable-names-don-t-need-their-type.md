---
content: ''
cover: ''
date: 2020-04-08
datetime: 2020-04-08 00:00:00+00:00
description: So often I see a variables  So often I see a variables  Pandas  Pandas  Sometimes
  vanilla structures too Sometimes vanilla structures too It It Always name your
long_description: 'So often I see a variables  So often I see a variables  Pandas  Pandas  Sometimes
  vanilla structures too Sometimes vanilla structures too It It Always name your containers
  plural, so that naming while iterating is simple. Always name your containers '
now: 2022-05-07 21:32:25.893551
path: pages/blog/variable-names-don-t-need-their-type.md
slug: variable-names-don-t-need-their-type
status: published
super_description: "So often I see a variables  So often I see a variables  Pandas
  \ Pandas  Sometimes vanilla structures too Sometimes vanilla structures too It It
  Always name your containers plural, so that naming while iterating is simple. Always
  name your containers plural, so that naming while iterating is simple. Before I
  start fights \U0001F94A in code review, am I inline here or just being pedantic?
  Before I start fights \U0001F94A in code review, am I inline here or just being
  pedantic?"
tags:
- python
- dicuss
templateKey: blog-post
title: Variables names don't need their type
today: 2022-05-07
year: 2020
---

So often I see a variables `type()` inside of its name and it hurts me a little
inside.  Tell me I'm right or prove me wrong below.

## Examples

Pandas `DataFrames` are probably the worst offender that I see

``` python
# bad
sales_df = get_sales()

# good
sales = get_sales()
```

Sometimes vanilla structures too!

``` python
# bad
items_list = ['sneakers', 'pencils', 'paper', ]

# good
items = ['sneakers', 'pencils', 'paper', ]
```

## Edge Cases?

It's so common when you need to get inside a data structure in a special way that itsn't provided by the library.... I am not exactly sure of a good way around it.

``` python
# bad ??
sales = get_sales()
sales_dict = sales.to_dict()

# good
🤷‍♀️
```

## Containers are plural

Always name your containers plural, so that naming while iterating is simple.

``` python
prices = {}
items = ['sneakers', 'pencils', 'paper', ]
for item in items:
   prices[item] = get_price(item)
```

Before I start fights 🥊 in code review, am I inline here or just being pedantic?