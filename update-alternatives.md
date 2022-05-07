---
content: ''
cover: ''
date: 2021-11-20
datetime: 2021-11-20 00:00:00+00:00
description: ''
long_description: ''
now: 2022-05-07 21:32:25.892676
path: pages/blog/update-alternatives.md
slug: update-alternatives
status: draft
super_description: ''
tags:
- linux
- bash
templateKey: blog-post
title: Update Alternatives in Linux
today: 2022-05-07
year: 2021
---

``` bash
update-alternatives --query python
```

``` bash
update-alternatives: error: no alternatives for python
```

``` bash
sudo update-alternatives --install /usr/local/bin/python python `which python3.8` 2
# update-alternatives: using /usr/bin/python3.8 to provide /usr/local/bin/python (python) in auto mode

sudo update-alternatives --install /usr/local/bin/python python `which python2.7` 5
# update-alternatives: using /usr/bin/python2.7 to provide /usr/local/bin/python (python) in auto mode

update-alternatives --query python
# Name: python
# Link: /usr/local/bin/python
# Status: auto
# Best: /usr/bin/python2.7
# Value: /usr/bin/python2.7
# 
# Alternative: /usr/bin/python2.7
# Priority: 5
# 
# Alternative: /usr/bin/python3.8
# Priority: 2

sudo update-alternatives --install /usr/local/bin/python python `which python3.8` 20
# update-alternatives: using /usr/bin/python3.8 to provide /usr/local/bin/python (python) in auto mode
```