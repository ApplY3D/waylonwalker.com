---
content: ''
cover: ''
date: 2021-04-05
datetime: 2021-04-05 00:00:00+00:00
description: Testing print/log statements in pytest can be a bit tricky, capsys makes
  it Testing print/log statements in pytest can be a bit tricky, capsys makes it capsys
  i
long_description: Testing print/log statements in pytest can be a bit tricky, capsys
  makes it Testing print/log statements in pytest can be a bit tricky, capsys makes
  it capsys is a builtin pytest fixture that can be passed into any test to capture
  capsys is a builtin
now: 2022-05-07 21:32:25.894416
path: pages/blog/pytest-capsys.md
slug: pytest-capsys
status: published
super_description: Testing print/log statements in pytest can be a bit tricky, capsys
  makes it Testing print/log statements in pytest can be a bit tricky, capsys makes
  it capsys is a builtin pytest fixture that can be passed into any test to capture
  capsys is a builtin pytest fixture that can be passed into any test to capture Simply
  create a test function that accepts capsys as an argument and pytest Simply create
  a test function that accepts capsys as an argument and pytest
tags:
- python
templateKey: blog-post
title: Pytest capsys
today: 2022-05-07
year: 2021
---

Testing print/log statements in pytest can be a bit tricky, capsys makes it
super easy, but I often struggle to find it.


## capsys

capsys is a builtin pytest fixture that can be passed into any test to capture
stdin/stdout.  For a more comprehensive description check out the docs on
[capsys](https://docs.pytest.org/en/stable/capture.html#accessing-captured-output-from-a-test-function)

## using capsys

Simply create a test function that accepts capsys as an argument and pytest
will give you a capsys opject.

```python
def test_print(capsys):
    print('hello')
    captured = capsys.readouterr()
    assert 'hello' in captured.out
    print('world')
    captured = capsys.readouterr()
    assert 'world' in captured.out
```