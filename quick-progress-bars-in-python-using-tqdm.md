---
content: ''
cover: ''
date: 2019-09-18
datetime: 2019-09-18 00:00:00+00:00
description: Quick Progress Bars in python using TQDM
long_description: tqdm is one of my favorite general purpose utility libraries in
  python.  It tqdm is one of my favorite general purpose utility libraries in python.  It
  for more gifs like these follow me on twitter for more gifs like these follow me
  on twitter TQDM a
now: 2022-05-07 21:32:25.892524
path: pages/blog/quick-progress-bars-in-python-using-tqdm.md
slug: quick-progress-bars-in-python-using-tqdm
status: published
super_description: 'tqdm is one of my favorite general purpose utility libraries in
  python.  It tqdm is one of my favorite general purpose utility libraries in python.  It
  for more gifs like these follow me on twitter for more gifs like these follow me
  on twitter TQDM also has a convenience function called trange that wraps the range
  function with a tqdm progress bar automatically. TQDM also has a convenience function
  called trange that wraps the range function with a tqdm progress bar automatically.
  There is also '
tags:
- python
templateKey: blog-post
title: Quick Progress Bars in python using TQDM
today: 2022-05-07
year: 2019
---

tqdm is one of my favorite general purpose utility libraries in python.  It
allows me to see progress of multipart processes as they happen.  I really like
this for when I am developing something that takes some amount of time and I am
unsure of performance.  It allows me to be patient when the process is going
well and will finish in sufficient time, and allows me to 💥 kill it and find a
way to make it perform better if it will not finish in sufficient time.

![](/tqdm2.gif)

> for more gifs like these follow me on twitter
[@waylonwalker](https://twitter.com/_WaylonWalker)

**Add a simple Progress bar!**
```python
from tqdm import tqdm
from time import sleep

for i in tqdm(range(10)):
	sleep(1)
```

**convenience**

TQDM also has a convenience function called trange that wraps the range function with a tqdm progress bar automatically.

```python
from tqdm import trange
from time import sleep

for i in trange(range(10)):
	sleep(1)
```


**notebook support**

There is also notebook support.  If you are bouncing between ipython and jupyter I recomend importing from the auto module.

```python
from tqdm.auto import tqdm
from time import sleep

for i in tqdm(range(10)):
	sleep(1)
```


  <div class="onelinelink-wrapper">
      <a class="onelinelink" href="https://waylonwalker.com/autoreload-ipython/">
          <img style="float: right;" align='right' src="https://images.waylonwalker.com/autoreload-ipython-og_250x140.png" alt="article cover for 
 Autoreload in Ipython
"/>
          <p><strong>
 Autoreload in Ipython
</strong></p>
      </a>
  </div>


> If you are using notebooks you should enable ipython autoreload 👆