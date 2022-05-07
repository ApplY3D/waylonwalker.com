---
content: ''
cover: ''
date: 2021-09-13
datetime: 2021-09-13 00:00:00+00:00
description: https://youtu.be/-gEwU-MrPuA https://youtu.be/-gEwU-MrPuA Before we jump
  in with anything crazy, let Before we jump in with anything crazy, let You will
  need to
long_description: https://youtu.be/-gEwU-MrPuA https://youtu.be/-gEwU-MrPuA Before
  we jump in with anything crazy, let Before we jump in with anything crazy, let You
  will need to import node from kedro.pipeline to start creating nodes. You will need
  to import node fro
now: 2022-05-07 21:32:25.894027
path: pages/blog/kedro-your-first-nodes.md
slug: kedro-your-first-nodes
status: published
super_description: 'https://youtu.be/-gEwU-MrPuA https://youtu.be/-gEwU-MrPuA Before
  we jump in with anything crazy, let Before we jump in with anything crazy, let You
  will need to import node from kedro.pipeline to start creating nodes. You will need
  to import node from kedro.pipeline to start creating nodes. The  The  Inputs and
  outputs can be None, a single catalog entry as a string, mutiple Inputs and outputs
  can be None, a single catalog entry as a string, mutiple Sometimes in our pipelines
  our data is coming '
tags:
- kedro
- python
templateKey: blog-post
title: Writing your first kedro Nodes
today: 2022-05-07
year: 2021
---

https://youtu.be/-gEwU-MrPuA

Before we jump in with anything crazy, let's make some nodes with some vanilla
data structures.

## import node

You will need to import node from kedro.pipeline to start creating nodes.

``` python
from kedro.pipeline import node
```

## func

The `func` is a callable that will take the `inputs` and create the `outputs`.

## inputs / outputs

Inputs and outputs can be None, a single catalog entry as a string, mutiple
catalog entries as a List of strings, or a dictionary of strings where the key
is the keyword argument of the func and the value is the catalog entry to use
for that keyword.

## our first node

Sometimes in our pipelines our data is coming from an api where we already have
python functions built to pull with.  Thats ok, kedro supposrts that with
`inputs=None`.

``` python
def create_range():
    return range(100)

make_range = node(
    func=create_range,
    inputs=None,
    outputs='range'
    )
```

## second node

Now we have some data to work from, lets use that as our input.

``` python
def square_range():
    return [i**2 for i in range]

square_range = node(
    func=square_range,
    inputs='range',
    outputs='range_squared'
    )
```

## Multiple Inputs

Kedro can take lists or dicts as either input or output when your function
needs more than one input or output.


``` python
def concat(range, range_two):
    return [*range, *range_two]

concat_ranges = node(
    func=concat,
    inputs=['range', 'range_squared']
    outputs='concat'
    )

## inputs could also be defined as a dict
concat_ranges = node(
    func=concat,
    inputs={'range': 'range', 'range_two': 'range_squared'}
    outputs='concat'
    )
```

## Links

* [all of my kedro articles](https://waylonwalker.com/kedro/)
* [kedro playlist on YouTube](https://www.youtube.com/watch?v=bw5_FWDVRpU&list=PLTRNG6WIHETCoPt5gAKYSH_HCZvE_r41n)
* [node docs](https://kedro.readthedocs.io/en/stable/kedro.pipeline.node.html)
* [first_nodes.py](https://gist.github.com/WaylonWalker/347b32c6ae7b799d1e0853c3811a98de)