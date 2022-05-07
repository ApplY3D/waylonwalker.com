---
canonical_url: https://waylonwalker.com/hot_tips/026/
cover_image: https://images.waylonwalker.com/hot_tips/026.png
description: setup setup convert convert
published: true
tags:
- cli
- bash
title: 026.md
---

# Convert **Markdown** to _reveal.js_ slides

setup
``` bash
wget https://github.com/hakimel/reveal.js/archive/master.tar.gz tar -xzvf master.tar.gz mv reveal.js-master reveal.js
```

convert
``` bash
pandoc -t revealjs -s\
   -o myslides.html myslides.md \
   -V revealjs-url=https://unpkg.com/reveal.js@3.9.2/
```