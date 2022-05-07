---
content: ''
cover: ''
date: 2022-02-08
datetime: 2022-02-08 00:00:00+00:00
description: A super useful tool when doing PR A super useful tool when doing PR It
  It
long_description: A super useful tool when doing PR A super useful tool when doing
  PR It It
now: 2022-05-07 21:32:25.891877
path: pages/til/ag-ahead.md
slug: til/ag-ahead
status: published
super_description: A super useful tool when doing PR A super useful tool when doing
  PR It It
tags:
- cli
- bash
- linux
templateKey: til
title: ag silver searcher look ahead and look behind
today: 2022-05-07
year: 2022
---

A super useful tool when doing PR's or checking your own work during a big
refactor is the silver searcher.  Its a super fast command line based searching
tool. You just run `ag "<search term>"` to search for your search term.  This
will list out every line of every file in any directory under your current
working directory that contains a match.

## Ahead/Behind

It's often useful to need some extra context around the change.  I recently
reviewed a bunch of PR's that moved schema from `save_args` to the root of the
dataset in all yaml configs.  To ensure they all made it to the top level
DataSet configuraion, and not underneath save_args.  I can do a search for all
the schemas, and ensure that none of them are under `save_args` anymore.

``` bash
ag "schema: " -A 12 -B 12
```