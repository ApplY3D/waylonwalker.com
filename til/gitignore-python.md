---
content: ''
cover: ''
date: 2022-01-17
datetime: 2022-01-17 00:00:00+00:00
description: Many tools such as ripgrep respect the  Many tools such as ripgrep respect
  the  Editors like vscode often do not include files that are .gitignored in Editors
  l
long_description: Many tools such as ripgrep respect the  Many tools such as ripgrep
  respect the  Editors like vscode often do not include files that are .gitignored
  in Editors like vscode often do not include files that are .gitignored in pathspec
  pathspec pathspec p
now: 2022-05-07 21:32:25.891869
path: pages/til/gitignore-python.md
slug: til/gitignore-python
status: published
super_description: Many tools such as ripgrep respect the  Many tools such as ripgrep
  respect the  Editors like vscode often do not include files that are .gitignored
  in Editors like vscode often do not include files that are .gitignored in pathspec
  pathspec pathspec pathspec
tags:
- python
templateKey: til
title: Python Respect the .gitignore
today: 2022-05-07
year: 2022
---

Many tools such as ripgrep respect the `.gitignore` file in the directory
it's searching in.  This helps make it incredibly faster and generally
more intuitive for the user as it just searches files that are part of
thier project and not things like their virtual environments, node
modules, or compiled builds.

> Editors like vscode often do not include files that are .gitignored in
> their search either.

`pathspec` is a pattern matching library that implements git's wildmatch
pattern so that you can ignore files included in your `.gitignore`
patterns.  You might want this to help make your libraries more
performant, or more intuitive for you users.

```python
import pathspec
from pathlib import Path

markdown_files = Path().glob('**/*.md')
if (Path(".gitignore").exists():
    lines = Path(".gitignore").read_text().splitlines()

    spec = pathspec.PathSpec.from_lines("gitwildmatch", lines)

    markdown_files = [
        file for file in markdown_files if not spec.match_file(str(file))
    ]
```

`pathspec` [home page](https://github.com/cpburnz/python-path-specification)