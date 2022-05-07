---
canonical_url: https://waylonwalker.com/pytest-capsys/
cover_image: https://images.waylonwalker.com/pytest-capsys.png
description: Testing print/log statements in pytest can be a bit tricky, capsys makes
  it Testing print/log statements in pytest can be a bit tricky, capsys makes it capsys
  i
published: true
tags:
- python
title: Pytest capsys
---

Testing print/log statements in pytest can be a bit tricky, capsys makes it super easy, but I often struggle to find it.


## capsys

capsys is a builtin pytest fixture that can be passed into any test to capture stdin/stdout.  For a more comprehensive description check out the docs on [capsys](https://docs.pytest.org/en/stable/capture.html#accessing-captured-output-from-a-test-function)

## using capsys

Simply create a test function that accepts capsys as an argument and pytest will give you a capsys opject.

```python
def test_print(capsys):
    print('hello')
    captured = capsys.readouterr()
    assert 'hello' in captured.out
    print('world')
    captured = capsys.readouterr()
    assert 'world' in captured.out
```