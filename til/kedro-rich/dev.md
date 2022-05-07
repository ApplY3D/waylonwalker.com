---
canonical_url: https://waylonwalker.com/til/kedro-rich/
cover_image: https://images.waylonwalker.com/til/kedro-rich.png
description: Kedro rich is a very new and unstable (it Kedro rich is a very new and
  unstable (it There is no pypi package yet, but it There is no pypi package yet,
  but it Yo
published: true
tags:
- python
- kedro
- cli
title: Make Kedro Runs Beautiful
---

Kedro rich is a very new and unstable (it's good, just not ready) plugin for kedro to make the command line prettier.

## Install kedro rich

There is no pypi package yet, but it's on github.  You can pip install it with the git url.

``` bash
pip install git+https://github.com/datajoely/kedro-rich
```

## Kedro run

You can run your pipeline just as you normally would, except you get progress bars and pretty prints.

```
kedro run
```

![kedro rich pretty run](https://images.waylonwalker.com/kedro-rich-run.png)


## Kedro catalog

Listing out catalog entries from the command line now print out a nice pretty table.

``` bash
kedro catalog list
```

![kedro rich catalog list table output](https://images.waylonwalker.com/kedro-rich-catalog-list.png)

## Give it a star

Go to the [GitHub repo](https://github.com/datajoely/kedro-rich) and give it a star, Joel deserves it.