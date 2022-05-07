---
content: ''
cover: ''
date: 2022-04-30
datetime: 2022-04-30 00:00:00+00:00
description: GitPython GitPython I recently made myself a handy tool for making screenshots
  in python and it I recently made myself a handy tool for making screenshots in py
long_description: GitPython GitPython I recently made myself a handy tool for making
  screenshots in python and it I recently made myself a handy tool for making screenshots
  in python and it https://waylonwalker.com/screenshot-to-blog/ https://waylonwalker.com/screensh
now: 2022-05-07 21:32:25.891516
path: pages/til/python-git.md
slug: til/python-git
status: published
super_description: GitPython GitPython I recently made myself a handy tool for making
  screenshots in python and it I recently made myself a handy tool for making screenshots
  in python and it https://waylonwalker.com/screenshot-to-blog/ https://waylonwalker.com/screenshot-to-blog/
  GitPython GitPython Import Repo from the git library and create an instance of the  Import
  Repo from the git library and create an instance of the  from the docs from the
  docs It provides abstractions of git objects for easy access of rep
tags:
- python
- cli
- git
templateKey: til
title: Using Git from Python
today: 2022-05-07
year: 2022
---

`GitPython` is a python api for your git repos, it can be quite handy when you
need to work with git from python.

## Use Case

I recently made myself a handy tool for making screenshots in python and it
need to do a git commit and push from within the script.  For this I reached
for `GitPython`.


  <div class="onelinelink-wrapper">
      <a class="onelinelink" href="https://waylonwalker.com/screenshot-to-blog/">
          <img style="float: right;" align='right' src="https://images.waylonwalker.com/screenshot-to-blog-og_250x140.png" alt="article cover for 
 How I Quickly Capture Screenshots directly into My Blog
"/>
          <p><strong>
 How I Quickly Capture Screenshots directly into My Blog
</strong></p>
      </a>
  </div>


## Installation

`GitPython` is a python library hosted on pypi that we will want to install
into our virtual environments using pip.

``` python
pip install GitPython
```

## Create a Repo Object

Import Repo from the git library and create an instance of the `Repo` object by
giving it a path to the directory containing your `.git` directory.

``` python
from git import Repo
repo = Repo('~/git/waylonwalker.com/')
```

## Two interfaces

from the docs

> It provides abstractions of git objects for easy access of repository data,
> and additionally allows you to access the git repository more directly using
> either a pure python implementation, or the faster, but more resource
> intensive git command implementation.

I only needed to use the more intensive but familar to me git command
implementation to get me project off the ground.  There is a good
[tutorial](https://gitpython.readthedocs.io/en/stable/tutorial.html#tutorial-label)
to get you started with their pure python implementation in their docs.

## Status

Requesting the git status can be done as follows.

> note I have prefixed my commands with >>> to distinguish between the command
> I entered and the output.

```
>>> print(repo.git.status())

On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        blog/
```

You can even pass in flags that you would pass into the cli.

```
>>> print(repo.git.status("-s"))
?? blog/
```

## log

Example of using the log.

``` python
print(repo.git.log('--oneline', '--graph'))

* 0d28bd8 fix broken image link
* 3573928 wip screenshot-to-blog
* fed9abc wip screenshot-to-blog
* d383780 update for wsl2
* ad72b14 wip screenshot-to-blog
* 144c2f3 gratitude-180
```

## Find Deleted Files

We can even do things like find all files that have been deleted and the hash
they were deleted.

``` python
print(repo.git.log('--diff-filter', 'D', '--name-only', '--pretty=format:"%h"'))
```

https://waylonwalker.com/git-find-deleted-files/

> full post on finding deleted files

## My Experience

This library seemed pretty straightforward and predicatable once I realized
there were two main implementations and that I would already be familar with
the more intensive git command implementation.