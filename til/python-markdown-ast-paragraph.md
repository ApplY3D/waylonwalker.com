---
content: ''
cover: ''
date: 2022-02-05
datetime: 2022-02-05 00:00:00+00:00
description: In looking for a way to automatically generate descriptions for pages
  I In looking for a way to automatically generate descriptions for pages I It It
long_description: In looking for a way to automatically generate descriptions for
  pages I In looking for a way to automatically generate descriptions for pages I
  It It
now: 2022-05-07 21:32:25.891950
path: pages/til/python-markdown-ast-paragraph.md
slug: til/python-markdown-ast-paragraph
status: published
super_description: In looking for a way to automatically generate descriptions for
  pages I In looking for a way to automatically generate descriptions for pages I
  It It
tags:
- python
- webdev
templateKey: til
title: Using a Python Markdown ast to Find All Paragraphs
today: 2022-05-07
year: 2022
---

In looking for a way to automatically generate descriptions for pages I
stumbled into a markdown ast in python.  It allows me to go over the
markdown page and get only paragraph text.  This will ignore headings,
blockquotes, and code fences.


``` python
import commonmark
parser = commonmark.Parser()
ast = parser.parse(p.content)

paragraphs = ''
for node in ast.walker():
    if node[0].t == "paragraph":
        paragraphs += " "
        paragraphs += node[0].first_child.literal
```

It's also super fast, previously I was rendering to html and using
beautifulsoup to get only the paragraphs.  Using the commonmark ast was
about 5x faster on my site.