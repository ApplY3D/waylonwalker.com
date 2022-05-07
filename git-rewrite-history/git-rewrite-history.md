---
content: ''
cover: ''
date: 2019-02-05
datetime: 2019-02-05 00:00:00+00:00
description: rebase rebase git commit --amend git commit --amend rage quit rage quit
  git reset HEAD~n  git reset HEAD~n  removes modifications removes modifications
  keeps hi
long_description: rebase rebase git commit --amend git commit --amend rage quit rage
  quit git reset HEAD~n  git reset HEAD~n  removes modifications removes modifications
  keeps hitsory of changes and undoes them keeps hitsory of changes and undoes them
  git checkout HEA
now: 2022-05-07 21:32:25.894704
path: pages/blog/git-rewrite-history/git-rewrite-history.md
slug: git-rewrite-history/git-rewrite-history
status: published
super_description: rebase rebase git commit --amend git commit --amend rage quit rage
  quit git reset HEAD~n  git reset HEAD~n  removes modifications removes modifications
  keeps hitsory of changes and undoes them keeps hitsory of changes and undoes them
  git checkout HEAD~n --  git checkout HEAD~n --  keeps modifications keeps modifications
  removes history removes history --SOFT --SOFT --HARD --HARD --Mixed --Mixed locally
  before push locally before push after push after push after push after push
tags:
- git
templateKey: blog-post
title: Rewrite History with Git
today: 2022-05-07
year: 2019
---

* rebase
* git commit --amend

## Unstage learning-python-debugger

``` bash
git reset -- <file>
```

**rage** unstage to wipte out history of staged commit
``` bash
git reset --hard <file>
```

## Undo file

* rage quit
* git reset HEAD~n <file>
    * removes modifications
    * keeps hitsory of changes and undoes them
* git checkout HEAD~n -- <file>
    * keeps modifications
    * removes history

    * --SOFT
    * --HARD
    * --Mixed

## undo n commits back

locally before push
``` bash
git reset HEAD~n
```

after push
``` bash
git revert HEAD~n
```

## update .gitignore

after push
``` bash
git rm -r --cached .
git commit -am "Updated .gitignore"
```