---
content: ''
cover: ''
date: 2019-02-10
datetime: 2019-02-10 00:00:00+00:00
description: How to setup a data science project in python.
long_description: 'Use  Use  Add a minimal  Add a minimal  consider using  consider
  using '
now: 2022-05-07 21:32:25.894711
path: pages/blog/bit-01/bit_01.md
slug: bit-01/bit_01
status: draft
super_description: 'Use  Use  Add a minimal  Add a minimal  consider using  consider
  using '
tags: []
templateKey: blog-post
title: Minimal Project Structure
today: 2022-05-07
year: 2019
---

## TLDR

Use **[.gitignore.io](https://www.gitignore.io)** and consider adding an alias to your terminal to quickly add a .gitignore to any project missing one.

``` bash
alias gitignore='curl https://www.gitignore.io/api/vim,emacs,python,pycharm,sublimetext,visualstudio,visualstudiocode,data > .gitignore'
```

Add a minimal **setup.py** to the root of your project, and use the following command to install it.

``` bash
pip install -e .
```

consider using **[cookiecutter](https://github.com/audreyr/cookiecutter)