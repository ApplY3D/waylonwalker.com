---
content: ''
cover: ''
date: 2022-02-12
datetime: 2022-02-12 00:00:00+00:00
description: In python, a string is a string until you add special characters. In
  python, a string is a string until you add special characters. In browsing twitter
  this mor
long_description: In python, a string is a string until you add special characters.
  In python, a string is a string until you add special characters. In browsing twitter
  this morning I came accross this tweet, that showed that In browsing twitter this
  morning I came a
now: 2022-05-07 21:32:25.891725
path: pages/til/python-string-is-string.md
slug: til/python-string-is-string
status: published
super_description: In python, a string is a string until you add special characters.
  In python, a string is a string until you add special characters. In browsing twitter
  this morning I came accross this tweet, that showed that In browsing twitter this
  morning I came accross this tweet, that showed that https://twitter.com/bascodes/status/1492147596688871424
  https://twitter.com/bascodes/status/1492147596688871424 I popped open ipython to
  play with this.  I could confirm on  I popped open ipython to play with this.
tags:
- python
templateKey: til
title: Python string of letters is a string of letters, but not with special
today: 2022-05-07
year: 2022
---

In python, a string is a string until you add special characters.

In browsing twitter this morning I came accross this tweet, that showed that
you can use `is` accross two strings if they do not contain special characters.

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">🐍 Python:<br>- Allocate all numbers from -5 to 256 on startup<br>- Intern all strings up to a length of 3 but only digits and letters<br><br>⚡️ Also Python:<br>- Explicit is better than implicit.<br>- Special cases aren&#39;t special enough to break the rules. <a href="https://t.co/SlZRFcQoQK">pic.twitter.com/SlZRFcQoQK</a></p>&mdash; Bas codes (@bascodes) <a href="https://twitter.com/bascodes/status/1492147596688871424?ref_src=twsrc%5Etfw">February 11, 2022</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>


I popped open ipython to play with this.  I could confirm on `3.9.7`, short
strings that I typed in worked as expected.

``` python
waylonwalker ↪main v3.9.7 ipython
❯ a = "asdf"

waylonwalker ↪main v3.9.7 ipython
❯ b = "asdf"

waylonwalker ↪main v3.9.7 ipython
❯ a is b
True
```

Using the `upper()` method on these strings does break down.

``` python
waylonwalker ↪main v3.9.7 ipython
❯ a.upper() is b.upper()
False

waylonwalker ↪main v3.9.7 ipython
❯ a = "ASDF"

waylonwalker ↪main v3.9.7 ipython
❯ b = "ASDF"

waylonwalker ↪main v3.9.7 ipython
❯ a is b
True
```

If You can also see this in the id of the objects as well, which is the memmory
address in CPython.

``` python
waylonwalker ↪main v3.9.7 ipython
❯ id(a)
140717359289568

waylonwalker ↪main v3.9.7 ipython
❯ id(b)
140717359289568

waylonwalker ↪main v3.9.7 ipython
❯ id(a.upper())
140717359581824

waylonwalker ↪main v3.9.7 ipython
❯ id(b.upper())
140717360337824
```

Finally just as the post shows if you add a special character in there it also
breaks.

``` python
waylonwalker ↪main v3.9.7 ipython
❯ a = "ASDF!"

waylonwalker ↪main v3.9.7 ipython
❯ b = "ASDF!"

waylonwalker ↪main v3.9.7 ipython
❯ a is b
False
```

## What should you do

First and foremost, these are the exact pitfalls that `flake8` guards you
against.  So the very first things you should take away here is that there is a
lot of wisdom and value in `flake8`.

Second, the `is` comparison should be used for things that you want to compare
to exact memmory addresses.  These include booleans and None.  Don't use `is`
accross two assigned variables.