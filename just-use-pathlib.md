---
content: ''
cover: ''
date: 2019-09-26
datetime: 2019-09-26 00:00:00+00:00
description: Pathlib is an amazing cross-platform path tool.
long_description: Pathlib is an amazing cross-platform path tool. Pathlib is an amazing
  cross-platform path tool.
now: 2022-05-07 21:32:25.892366
path: pages/notes/just-use-pathlib.md
slug: just-use-pathlib
status: published
super_description: Pathlib is an amazing cross-platform path tool. Pathlib is an amazing
  cross-platform path tool.
tags:
- python
templateKey: blog-post
title: Just Use Pathlib
today: 2022-05-07
year: 2019
---

Pathlib is an amazing cross-platform path tool.

## Import

```python
from pathlib import Path
```

## Create path object

**Current Directory**

```python
cwd = Path('.').absolute()
```

**Users Home Directory**

```python
home = Path.home()
```

**module directory**

```python
module_path = Path(__file__)
```

**Others**
Let's create a path relative to our current module.

```python
data_path = Path(__file__) / 'data'
```

## Check if files exist

## Make Directories

```python
data_path.mkdir(parents=True, exists_ok=True)
```

## rename files

```python
Path(data_path /'example.csv').rename('real.csv')
```

## List files

## Glob Files

```python
data_path.glob('*.csv')
```

**recursively**

```python
data_path.rglob('*.csv')
```

## Write

```python
Path(data_path / 'meta.txt').write_text(f'created on {datetime.datetime.today()})
```