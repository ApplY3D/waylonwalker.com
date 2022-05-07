---
canonical_url: https://waylonwalker.com/quick-progress-bars-in-python-using-tqdm/
cover_image: https://images.waylonwalker.com/quick-progress-bars-in-python-using-tqdm.png
description: Quick Progress Bars in python using TQDM
published: true
tags:
- python
title: Quick Progress Bars in python using TQDM
---

tqdm is one of my favorite general purpose utility libraries in python.  It allows me to see progress of multipart processes as they happen.  I really like this for when I am developing something that takes some amount of time and I am unsure of performance.  It allows me to be patient when the process is going well and will finish in sufficient time, and allows me to 💥 kill it and find a way to make it perform better if it will not finish in sufficient time.

![](/tqdm2.gif)

> for more gifs like these follow me on twitter
[@waylonwalker](https://twitter.com/_WaylonWalker)

**Add a simple Progress bar!**
```python
from tqdm import tqdm from time import sleep

for i in tqdm(range(10)):
	sleep(1)
```

**convenience**

TQDM also has a convenience function called trange that wraps the range function with a tqdm progress bar automatically.

```python
from tqdm import trange from time import sleep

for i in trange(range(10)):
	sleep(1)
```


**notebook support**

There is also notebook support.  If you are bouncing between ipython and jupyter I recomend importing from the auto module.

```python
from tqdm.auto import tqdm from time import sleep

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