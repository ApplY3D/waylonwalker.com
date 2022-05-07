---
canonical_url: https://waylonwalker.com/til/python-markdown-ast-paragraph/
cover_image: https://images.waylonwalker.com/til/python-markdown-ast-paragraph.png
description: In looking for a way to automatically generate descriptions for pages
  I In looking for a way to automatically generate descriptions for pages I It It
published: true
tags:
- python
- webdev
title: Using a Python Markdown ast to Find All Paragraphs
---

In looking for a way to automatically generate descriptions for pages I stumbled into a markdown ast in python.  It allows me to go over the markdown page and get only paragraph text.  This will ignore headings, blockquotes, and code fences.


``` python
import commonmark parser = commonmark.Parser() ast = parser.parse(p.content)

paragraphs = '' for node in ast.walker():
    if node[0].t == "paragraph":
        paragraphs += " "
        paragraphs += node[0].first_child.literal
```

It's also super fast, previously I was rendering to html and using beautifulsoup to get only the paragraphs.  Using the commonmark ast was about 5x faster on my site.