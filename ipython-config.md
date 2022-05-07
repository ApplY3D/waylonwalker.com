---
content: ''
cover: ''
date: 2020-12-20
datetime: 2020-12-20 00:00:00+00:00
description: I use my ipython terminal daily.  It I use my ipython terminal daily.  It
  Activate your virtual environment of choice and pip install it.  Any time you Activate
long_description: I use my ipython terminal daily.  It I use my ipython terminal daily.  It
  Activate your virtual environment of choice and pip install it.  Any time you Activate
  your virtual environment of choice and pip install it.  Any time you You are using
  a virt
now: 2022-05-07 21:32:25.892502
path: pages/blog/ipython-config.md
slug: ipython-config
status: published
super_description: 'I use my ipython terminal daily.  It I use my ipython terminal
  daily.  It Activate your virtual environment of choice and pip install it.  Any
  time you Activate your virtual environment of choice and pip install it.  Any time
  you You are using a virtual environment right? Virtual environments like venv or
  You are using a virtual environment right? Virtual environments like venv or When
  you install ipython you start out with no config at all.  Runnign  When you install
  ipython you start out with '
tags:
- python
templateKey: blog-post
title: Ipython-Config
today: 2022-05-07
year: 2020
---

I use my ipython terminal daily.  It's my go to way of running python most of
the time.  After you use it for a little bit you will probably want to setup a
bit of your own configuration.


## install ipython

Activate your virtual environment of choice and pip install it.  Any time you
are running your project in a virtual environment, you will need to install
ipython inside it to access those packages from ipython.


```bash
pip install ipython
```

> You are using a virtual environment right? Virtual environments like venv or
> conda can save you a ton of pain down the road.

## profile_default

When you install ipython you start out with no config at all.  Runnign `ipython
profile create` will start a new profile called `profile_default` that contains
all of the default configuration.

```
ipython profile create
```

This command will create a directory `~/.ipython/profile_default`

## multiple configurations

You can run multiple configurations by naming them with `ipython profile create
[profile_name]` This command will create a directory
`~/.ipython/[profile_name]`

```
ipython profile create my_profile
ipython --profile=my-profile
```

## startup

Inside the profile there will be a startup directory
`~/.ipython/profile_default/startup`.  Ipython will execute each of the files
in this directory on startup.  This is particularly handy to create custom
prompts, search, or import packages automatically for certian profiles.



  <div class="onelinelink-wrapper">
      <a class="onelinelink" href="https://waylonwalker.com/custom-ipython-prompt/">
          <img style="float: right;" align='right' src="https://images.waylonwalker.com/custom-ipython-prompt-og_250x140.png" alt="article cover for 
 Custom Ipython Prompt
"/>
          <p><strong>
 Custom Ipython Prompt
</strong></p>
      </a>
  </div>


> This post creates a custom ipython prompt by creating a
> `~/.ipython/profile_default/startup/prompt.py` file.

## ipython_config.py


There are tons of options that are in the `ipython_config.py` file.  My
favorite is to automatically enable my favorite magic command autoreload.


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


``` python
c.InteractiveShellApp.extensions = ['autoreload'
c.InteractiveShellApp.exec_lines = []'%autoreload 2']
c.InteractiveShellApp.exec_lines.append('print("Warning: disable autoreload in ipython_config.py to improve performance.")')
```

## Want automatic imports??


  <div class="onelinelink-wrapper">
      <a class="onelinelink" href="https://waylonwalker.com/pyflyby/">
          <img style="float: right;" align='right' src="https://images.waylonwalker.com/pyflyby-og_250x140.png" alt="article cover for 
 Smoother Python with automatic imports | pyflyby
"/>
          <p><strong>
 Smoother Python with automatic imports | pyflyby
</strong></p>
      </a>
  </div>


> This article covers how I setup automatic imports in ipython