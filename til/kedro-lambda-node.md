---
content: ''
cover: ''
date: 2022-01-31
datetime: 2022-01-31 00:00:00+00:00
description: I keep my nodes short and sweet.  They do one thing and do it well. I
  I keep my nodes short and sweet.  They do one thing and do it well. I Here are two
  example
long_description: 'I keep my nodes short and sweet.  They do one thing and do it well.
  I I keep my nodes short and sweet.  They do one thing and do it well. I Here are
  two examples, the first one  Here are two examples, the first one  Many times I
  just want to get the '
now: 2022-05-07 21:32:25.891491
path: pages/til/kedro-lambda-node.md
slug: til/kedro-lambda-node
status: published
super_description: 'I keep my nodes short and sweet.  They do one thing and do it
  well. I I keep my nodes short and sweet.  They do one thing and do it well. I Here
  are two examples, the first one  Here are two examples, the first one  Many times
  I just want to get the data in as fast as possible, learn Many times I just want
  to get the data in as fast as possible, learn Note: try not to take the idea of
  a one liner too far.  If your Note: try not to take the idea of a one liner too
  far.  If your'
tags:
- python
- kedro
templateKey: til
title: Lambda Function as a Kedro Node
today: 2022-05-07
year: 2022
---

I keep my nodes short and sweet.  They do one thing and do it well. I
turn almost every DataFrame transformation into its own node.  It makes
it must easier to pull catalog entries, than firing up the pipeline,
running it, and starting a debugger.  For this reason many of my nodes
can be built from inline lambdas.

## Examples

Here are two examples, the first one `lambda x: x` is sometimes referred
to as an identity function.  This is super common to use in the early
phases of a project.  It lets you follow standard layering conventions,
without skipping a layer, overthinking if you should have the layer or
not, and leaves a good placholder to fill in later when you need it.

> Many times I just want to get the data in as fast as possible, learn
> about it, then go back and tidy it up.

``` python
from kedro.pipeline import node

my_first_node = node(
   func=lambda x: x,
   inputs='raw_cars',
   output='int_cars',
   tags=['int',]
   )

my_first_node = node(
   func=lambda cars: cars[['mpg', 'cyl', 'disp',]].query('disp>200'),
   inputs='raw_cars',
   output='int_cars',
   tags=['pri',]
   )
```

> Note: try not to take the idea of a one liner too far.  If your
> one line function wraps several lines down it probably deserves to be
> a real function for readability and a good docstring.