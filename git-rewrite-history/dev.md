---
canonical_url: https://waylonwalker.com/git-rewrite-history/
cover_image: https://images.waylonwalker.com/git-rewrite-history.png
description: rebase rebase git commit --amend git commit --amend rage quit rage quit
  git reset HEAD~n  git reset HEAD~n  removes modifications removes modifications
  keeps hi
published: true
tags:
- git
title: Rewrite History with Git
---

* rebase
* git commit --amend

## Unstage

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
git rm -r --cached . git commit -am "Updated .gitignore"
```