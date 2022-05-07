---
content: ''
cover: ''
date: 2020-07-21
datetime: 2020-07-21 00:00:00+00:00
description: Mypy Mypy only uses pyproject.toml only uses pyproject.toml only uses
  pyproject.toml only uses pyproject.toml
long_description: Mypy Mypy only uses pyproject.toml only uses pyproject.toml only
  uses pyproject.toml only uses pyproject.toml
now: 2022-05-07 21:32:25.894604
path: pages/blog/how-python-tools-config.md
slug: how-python-tools-config
status: published
super_description: Mypy Mypy only uses pyproject.toml only uses pyproject.toml only
  uses pyproject.toml only uses pyproject.toml
tags:
- python
templateKey: blog-post
title: How python tools configure
today: 2022-05-07
year: 2020
---

## mypy

Mypy's config parser seems to be one of the most complex.  This is likely in part to it having the largest backwards compatability of all projects that I looked at.

[mypy/config_parser](https://github.com/python/mypy/blob/master/mypy/config_parser.py)


## flake8



[options/config.py](https://github.com/PyCQA/flake8/blob/master/src/flake8/options/config.py)

## black

[black](https://github.com/psf/black/blob/master/src/black/__init__.py#L277-L331)

## portray

* only uses pyproject.toml

[portray/config.py](https://github.com/timothycrosley/portray/blob/main/portray/config.py)

## interrogate

* only uses pyproject.toml