---
content: ''
cover: ''
date: 2021-08-22
datetime: 2021-08-22 00:00:00+00:00
description: Kedro pipeline create is a command that makes creating new Kedro pipeline
  create is a command that makes creating new https://youtu.be/HtyIKqlEoNw https://youtu
long_description: Kedro pipeline create is a command that makes creating new Kedro
  pipeline create is a command that makes creating new https://youtu.be/HtyIKqlEoNw
  https://youtu.be/HtyIKqlEoNw The kedro cli comes with the following command to scaffold
  out The kedro c
now: 2022-05-07 21:32:25.893709
path: pages/blog/kedro-pipeline-create.md
slug: kedro-pipeline-create
status: draft
super_description: Kedro pipeline create is a command that makes creating new Kedro
  pipeline create is a command that makes creating new https://youtu.be/HtyIKqlEoNw
  https://youtu.be/HtyIKqlEoNw The kedro cli comes with the following command to scaffold
  out The kedro cli comes with the following command to scaffold out The directory
  structure that it creates looks like this. The directory structure that it creates
  looks like this.
tags:
- kedro
- python
templateKey: blog-post
title: Kedro Pipeline Create
today: 2022-05-07
year: 2021
---

Kedro pipeline create is a command that makes creating new
pipelines much easier.  There is much less boilerplate that
you need to write yourself.

https://youtu.be/HtyIKqlEoNw

## creating a new pipeline

The kedro cli comes with the following command to scaffold out
new pipelines.  Note that it will not add it to your
`pipeline_registry`, to be covered later, you will need to add
it yourself.

``` bash
kedro pipeline create example
```

## results

The directory structure that it creates looks like this.

``` bash
tree src/kedro_conda/pipelines
src/kedro_conda/pipelines
├── __init__.py
└── example
    ├── __init__.py
    ├── nodes.py
    ├── pipeline.py
    └── README.md
```