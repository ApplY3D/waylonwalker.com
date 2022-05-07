---
author: Waylon S. Walker
content: ''
cover: ''
date: 2022-01-12
datetime: 2022-01-12 00:00:00+00:00
description: Converting markdown posts to pdf on ubuntu takes a few packages from
  the Converting markdown posts to pdf on ubuntu takes a few packages from the Here
  is an ima
long_description: Converting markdown posts to pdf on ubuntu takes a few packages
  from the Converting markdown posts to pdf on ubuntu takes a few packages from the
  Here is an image of what converting this article over to a pdf looks Here is an
  image of what converting
now: 2022-05-07 21:32:25.891862
path: pages/til/convert-markdown-pdf-linux.md
slug: til/convert-markdown-pdf-linux
status: published
super_description: Converting markdown posts to pdf on ubuntu takes a few packages
  from the Converting markdown posts to pdf on ubuntu takes a few packages from the
  Here is an image of what converting this article over to a pdf looks Here is an
  image of what converting this article over to a pdf looks
tags:
- linux
- blog
- cli
templateKey: til
title: Converting markdown to pdf with pandoc on linux
today: 2022-05-07
year: 2022
---

Converting markdown posts to pdf on ubuntu takes a few packages from the
standard repos.  I had to go through a few stack overflow posts, and
nothing seemed to have all the fonts and packages that I needed to
convert markdown, but this is what ended up working for me.

## Installing all the packages

``` bash
sudo apt install \
  pandoc \
  texlive-latex-base \
  texlive-fonts-recommended \
  texlive-extra-utils \
  texlive-latex-extra \
  texlive-xetex
```

## Using pandoc to convert markdown to a pdf.

``` python
# older versions of pandoc, I needed this one on ubuntu 18.04
pandoc pages/til/convert-markdown-pdf-linux.md -o convert-markdown-pdf.pdf --latex-engine=xelatex
# newer versions of pandoc, I needed this one on ubuntu 21.04
pandoc pages/til/convert-markdown-pdf-linux.md -o convert-markdown-pdf.pdf --pdf-engine=xelatex
```



![results of converting this post to a pdf](https://images.waylonwalker.com/convert-markdown-pdf-linux-result.png)

> Here is an image of what converting this article over to a pdf looks
> like.  The raw markdown is
> [here](https://waylonwalker.com/convert-markdown-pdf-linux.md).