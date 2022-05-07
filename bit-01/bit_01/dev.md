---
canonical_url: https://waylonwalker.com/bit-01/bit_01/
cover_image: https://images.waylonwalker.com/bit-01/bit_01.png
description: How to setup a data science project in python.
published: true
tags: []
title: Minimal Project Structure
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