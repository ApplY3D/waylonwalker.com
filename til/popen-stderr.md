---
content: ''
cover: ''
date: 2022-02-10
datetime: 2022-02-10 00:00:00+00:00
description: I often run shell commands from python with Popen, but not often enough
  I often run shell commands from python with Popen, but not often enough To get the
  stder
long_description: I often run shell commands from python with Popen, but not often
  enough I often run shell commands from python with Popen, but not often enough To
  get the stderr we must get it from the proc, read it, and decode the To get the
  stderr we must get it f
now: 2022-05-07 21:32:25.891915
path: pages/til/popen-stderr.md
slug: til/popen-stderr
status: published
super_description: 'I often run shell commands from python with Popen, but not often
  enough I often run shell commands from python with Popen, but not often enough To
  get the stderr we must get it from the proc, read it, and decode the To get the
  stderr we must get it from the proc, read it, and decode the Now that we can read
  the  Now that we can read the '
tags:
- python
templateKey: til
title: Read stderr from python subprocess.Popen
today: 2022-05-07
year: 2022
---

I often run shell commands from python with Popen, but not often enough
do I set up error handline for these subprocesses.  It's not too hard,
but it can be a bit awkward if you don't do it enough.

## Using Popen


``` python
import subprocess
from subprocess import Popen

# this will run the shell command `cat me` and capture stdout and stderr
proc = Popen(["cat", "me"], stdout=subprocess.PIPE, stderr=subprocess.PIPE)

# this will wait for the process to finish.
proc.wait()
```

## reading from stderr

To get the stderr we must get it from the proc, read it, and decode the
bystring.  Note that we can only get the stderr object once, so if you want to
do more than just read it you will need to store a copy of it.

``` python
proc.stderr.read().decode()
```

## Better Exception

Now that we can read the `stderr` we can make better error tracking for the
user so they can see what to do to resolve the issue rather than blindly
failing.

``` python
err_message = proc.stderr.read().decode()
if proc.returncode != 0:
    # the process was not successful

    if "No such file" in err_message:
        raise FileNotFoundError('No such file "me"')
```