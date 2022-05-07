---
content: ''
cover: ''
date: 2022-03-17
datetime: 2022-03-17 00:00:00+00:00
description: 'A very common task for any script is to look for files on the system.  My
  go to A very common task for any script is to look for files on the system.  My
  go to '
long_description: A very common task for any script is to look for files on the system.  My
  go to A very common task for any script is to look for files on the system.  My
  go to I setup a directory to make some examples about globbing.  Here is what the
  I setup a dire
now: 2022-05-07 21:32:25.891786
path: pages/til/python-pathlib-glob.md
slug: til/python-pathlib-glob
status: published
super_description: A very common task for any script is to look for files on the system.  My
  go to A very common task for any script is to look for files on the system.  My
  go to I setup a directory to make some examples about globbing.  Here is what the
  I setup a directory to make some examples about globbing.  Here is what the 1 directory,
  8 files 1 directory, 8 files Pathlib is a standard library module available in all
  LTS versions of python at Pathlib is a standard library module available in all
  LTS versions
tags:
- python
templateKey: til
title: How I glob for Files in Python
today: 2022-05-07
year: 2022
---

A very common task for any script is to look for files on the system.  My go to
method when globbing for files in python is to use pathlib.

## Setup

I setup a directory to make some examples about globbing.  Here is what the
directory looks like.

``` bash
❯ tree .
.
├── content
│   ├── hello.md
│   ├── hello.py
│   ├── me.md
│   └── you.md
├── readme.md
├── README.md
├── READMES.md
└── setup.py
```

1 directory, 8 files
## Pathlib

Pathlib is a standard library module available in all LTS versions of python at
this point.

``` python
❯ from pathlib import Path
```

Creating a Path instance.

``` python
# current working directory
Path()
Path.cwd()

# The users home directory
Path.home()

# Path to a directory by string
Path('/path/to/directory')

# The users ~/.config directory
Path.home() / '.config'
```

## Globbing Examples

The path object has a glob method that allows you to glob for files with a unix
style glob pattern to search for files.  Note that it gives you a generator.
This is great for many use cases, but for examples its easier to turn them to a
list to print them out.

If you need some more detail on what globbing is there is a
[wikipedia](https://en.wikipedia.org/wiki/Glob_(programming)) article
discussing it.  I am just showing how to glob with pathlib.

``` python

❯ Path().glob("**/*.md")
<generator object Path.glob at 0x7fa35adc4f90>

❯ list(Path().glob("**/*.md"))

[
    PosixPath('readme.md'),
    PosixPath('READMES.md'),
    PosixPath('README.md'),
    PosixPath('content/you.md'),
    PosixPath('content/me.md'),
    PosixPath('content/hello.md')
]

❯ list(Path().glob("**/*.py"))
[PosixPath('setup.py'), PosixPath('content/hello.py')]

❯ list(Path().glob("*.md"))
[PosixPath('readme.md'), PosixPath('READMES.md'), PosixPath('README.md')]

❯ list(Path().glob("*.py"))
[PosixPath('setup.py')]

❯ list(Path().glob("**/*hello*"))
[PosixPath('content/hello.py'), PosixPath('content/hello.md')]

❯ list(Path().glob("**/REA?ME.md"))
[PosixPath('README.md')]
```