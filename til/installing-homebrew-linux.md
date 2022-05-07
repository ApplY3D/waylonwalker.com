---
content: ''
cover: ''
date: 2021-12-29
datetime: 2021-12-29 00:00:00+00:00
description: Installing brew on linux proved quite easy and got pyenv running for
  me Installing brew on linux proved quite easy and got pyenv running for me I had
  never used
long_description: Installing brew on linux proved quite easy and got pyenv running
  for me Installing brew on linux proved quite easy and got pyenv running for me I
  had never used homebrew before, honestly I thought it was a mac only I had never
  used homebrew before, h
now: 2022-05-07 21:32:25.891462
path: pages/til/installing-homebrew-linux.md
slug: til/installing-homebrew-linux
status: published
super_description: Installing brew on linux proved quite easy and got pyenv running
  for me Installing brew on linux proved quite easy and got pyenv running for me I
  had never used homebrew before, honestly I thought it was a mac only I had never
  used homebrew before, honestly I thought it was a mac only That was it, now homebrew
  is working. Starting a new shell and running That was it, now homebrew is working.
  Starting a new shell and running
tags:
- linux
- bash
templateKey: til
title: Installing Homebrew on Linux
today: 2022-05-07
year: 2021
---

Installing brew on linux proved quite easy and got pyenv running for me
within 4 commands.

I had never used homebrew before, honestly I thought it was a mac only
thing for years.  Today I wanted to try out pyenv, and the reccommended
way to install was using homebrew.  I am not yet sure if I want either
in my normal workflow, so for now I am just going to pop open a new
terminal and install homebrew and see how it goes.


``` bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
echo 'eval "$(/home/linuxbrew/.linuxbrew/bin/brew shellenv)"' >> /home/walkers/.zprofile
eval "$(/home/linuxbrew/.linuxbrew/bin/brew shellenv)"
```

That was it, now homebrew is working. Starting a new shell and running
the command to install pyenv worked.

``` bash
brew install pyenv
```

## Links

* [homebrew](https://brew.sh/)