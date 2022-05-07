---
content: ''
cover: ''
date: 2021-10-10
datetime: 2021-10-10 00:00:00+00:00
description: We can We can https://youtu.be/TZrRAP-9UMk https://youtu.be/TZrRAP-9UMk
  In any python repl you can access the docstring of a function by calling for  In
  any pyt
long_description: We can We can https://youtu.be/TZrRAP-9UMk https://youtu.be/TZrRAP-9UMk
  In any python repl you can access the docstring of a function by calling for  In
  any python repl you can access the docstring of a function by calling for  In Ipython
  we can even
now: 2022-05-07 21:32:25.893644
path: pages/blog/ipython-help.md
slug: ipython-help
status: published
super_description: 'We can We can https://youtu.be/TZrRAP-9UMk https://youtu.be/TZrRAP-9UMk
  In any python repl you can access the docstring of a function by calling for  In
  any python repl you can access the docstring of a function by calling for  In Ipython
  we can even get some syntax highlighting with the  In Ipython we can even get some
  syntax highlighting with the  Sometimes the docstrings are not good enough, and
  don Sometimes the docstrings are not good enough, and don The more common way I
  do it is with the '
tags:
- python
templateKey: blog-post
title: Just Ask Ipython for help
today: 2022-05-07
year: 2021
---

## It happens to the best of us

We can't all remember every single function signature out there, it's just not
possible.  If you want to stay productive while coding without the temptation
to hit YouTube or Twitter.  Use the built in help.  Here are 5 ways to get help
without leaving your terminal.

https://youtu.be/TZrRAP-9UMk

## Docstrings

In any python repl you can access the docstring of a function by calling for `help`.

``` python
help(df.rolling)
```

In Ipython we can even get some syntax highlighting with the `?`.

``` python
df.rolling?
```

## Source Code

Sometimes the docstrings are not good enough, and don't give us the content we
need, and we just need to look at the source.  Without leaving your terminal
there are two ways I often use to get to the source of a function I am trying
to use.

``` python
import inspect
inspect.getsource(df.rolling)
```

The more common way I do it is with the ipython `??`.

```
df.rolling??
```

## Bonus rich.inspect

You thought the syntax highlighting was good with ipython, check out what
`rich.inspect` can do! As far as I know there is no way to get to source code,
but the results are still fantastic.



``` bash
pip install rich
```

> Install rich

``` python
from rich import inspect
inspect(cars.rolling, help=True)
```

> then inspect

## Connect with me

If you liked this one, check out the YouTube Channel, catch me live on twitch,
or connect on twitter, I'd love to hear from you.

twitter:  https://twitter.com/_WaylonWalker
twitch: https://www.twitch.tv/waylonwalker
github: https://github.com/waylonwalker/
twitch: https://www.twitch.tv/waylonwalker