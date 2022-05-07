---
canonical_url: https://waylonwalker.com/hot_tips/025/
cover_image: https://images.waylonwalker.com/hot_tips/025.png
description: setup setup convert convert
published: true
tags:
- cli
- bash
title: 025.md
---

# Convert **Markdown** to __reveal.js__ slides

setup
``` bash
wget https://github.com/hakimel/reveal.js/archive/master.tar.gz tar -xzvf master.tar.gz mv reveal.js-master reveal.js
```

convert
``` bash
pandoc -t revealjs -s -o myslides.html myslides.md -V revealjs-url=https://unpkg.com/reveal.js@3.9.2/
```