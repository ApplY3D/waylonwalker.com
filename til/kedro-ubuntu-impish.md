---
content: ''
cover: ''
date: 2022-01-02
datetime: 2022-01-02 00:00:00+00:00
description: I just installed a brand new Ubuntu 21.10 Impish Indri, and wanted a
  I just installed a brand new Ubuntu 21.10 Impish Indri, and wanted a But what I
  got back wa
long_description: 'I just installed a brand new Ubuntu 21.10 Impish Indri, and wanted
  a I just installed a brand new Ubuntu 21.10 Impish Indri, and wanted a But what
  I got back was not what I expected But what I got back was not what I expected This
  is weird, why cant '
now: 2022-05-07 21:32:25.892046
path: pages/til/kedro-ubuntu-impish.md
slug: til/kedro-ubuntu-impish
status: published
super_description: I just installed a brand new Ubuntu 21.10 Impish Indri, and wanted
  a I just installed a brand new Ubuntu 21.10 Impish Indri, and wanted a But what
  I got back was not what I expected But what I got back was not what I expected This
  is weird, why cant I run kedro new with pipx?  Lets try pip. This is weird, why
  cant I run kedro new with pipx?  Lets try pip. Same issue. Same issue. https://waylonwalker.com/what-is-kedro/
  https://waylonwalker.com/what-is-kedro/ Curious what kedro is?  Check out this
tags:
- kedro
- python
- datascience
templateKey: til
title: Running Kedro on Ubuntu 21.10 Impish Indri
today: 2022-05-07
year: 2022
---

I just installed a brand new Ubuntu 21.10 Impish Indri, and wanted a
kedro project to play with so I did what any good kedroid would do, I
went to my command line and ran

```
pipx run kedro new --starter spaceflights
```

But what I got back was not what I expected!

``` bash
Fatal error from pip prevented installation. Full pip output in file:
    /home/walkers/.local/pipx/logs/cmd_2022-01-01_20.42.16_pip_errors.log

Some possibly relevant errors from pip install:
    ERROR: Could not find a version that satisfies the requirement kedro (from versions: none)
    ERROR: No matching distribution found for kedro
Error installing kedro.
```

This is weird, why cant I run kedro new with pipx?  Lets try pip.

``` bash
pip install kedro
```

Same issue.

``` bash
ERROR: Could not find a version that satisfies the requirement kedro (from versions: none)
ERROR: No matching distribution found for kedro
```


  <div class="onelinelink-wrapper">
      <a class="onelinelink" href="https://waylonwalker.com/what-is-kedro/">
          <img style="float: right;" align='right' src="https://images.waylonwalker.com/what-is-kedro-og_250x140.png" alt="article cover for 
 What is Kedro
"/>
          <p><strong>
 What is Kedro
</strong></p>
      </a>
  </div>


> Curious what kedro is?  Check out this article.

## What's up..
_wrong python version_

The issue is that kedro only runs on up to `python 3.8`, and on Ubuntu
21.10 when you `apt install python3` you get `python 3.9` and the
standard repos don't have an old enough version to run kedro.

## How to fix this?

Theres a couple of ways you can fix this?  They all involve installing a
distribution that does not come from the standard repo.

## Where Can I get the right version

* Anaconda
* Python.org
* deadsnakes
* pyenv
* miniconda

## I have two articles that can help you


  <div class="onelinelink-wrapper">
      <a class="onelinelink" href="https://waylonwalker.com/install-miniconda/">
          <img style="float: right;" align='right' src="https://images.waylonwalker.com/install-miniconda-og_250x140.png" alt="article cover for 
 How to Install miniconda on linux (from the command line only)
"/>
          <p><strong>
 How to Install miniconda on linux (from the command line only)
</strong></p>
      </a>
  </div>


> Using miniconda

``` bash
conda create -n myenv python=3.8
```


  <div class="onelinelink-wrapper">
      <a class="onelinelink" href="https://waylonwalker.com/til/pyenv-first-impressions/">
          <img style="float: right;" align='right' src="https://images.waylonwalker.com/til/pyenv-first-impressions-og_250x140.png" alt="article cover for 
 My first impressions with pyenv
"/>
          <p><strong>
 My first impressions with pyenv
</strong></p>
      </a>
  </div>


> Using pyenv

``` bash
pyenv install 3.8.12
```