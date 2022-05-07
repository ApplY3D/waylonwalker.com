---
category: Blog
content: ''
cover: ''
date: 2018-05-16
datetime: 2018-05-16 00:00:00+00:00
description: none
long_description: I commonly have a need to paste the first few lines of a dataset
  into a markdown file.  I use two handy packages to do this,  I commonly have a need
  to paste the first few lines of a dataset into a markdown file.  I use two handy
  packages to do this,
now: 2022-05-07 21:32:25.894506
path: pages/blog/readme-tables.md
slug: readme-tables
status: draft
super_description: I commonly have a need to paste the first few lines of a dataset
  into a markdown file.  I use two handy packages to do this,  I commonly have a need
  to paste the first few lines of a dataset into a markdown file.  I use two handy
  packages to do this,  This is a super handy snippet that I use a lot.  Folks really
  appreciate it when they can see a sample of the data without opening the entire
  file. This is a super handy snippet that I use a lot.  Folks really appreciate it
  when they can see a samp
tags:
- data
- python
templateKey: blog-post
title: Generating Readme Tables From Pandas
today: 2022-05-07
year: 2018
---

## Generating Readme Tables From Pandas

I commonly have a need to paste the first few lines of a dataset into a markdown file.  I use two handy packages to do this, ```tabulate``` and ```pyperclip```.  Lets say I have a Pandas DataFrame in memory as ```df``` already.  All I would need to do to convert the first 5 rows to markdown and copy it to the clipboard is the following.

```Python
from tabulate import tabulate
import pyperclip
md = tabulate.tabulate(df.head(), df.columns, tablefmt='pipe')
pyperclip.copy(md)
```


This is a super handy snippet that I use a lot.  Folks really appreciate it when they can see a sample of the data without opening the entire file.