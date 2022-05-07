---
content: ''
cover: ''
date: 2022-01-15
datetime: 2022-01-15 00:00:00+00:00
description: When running a python process that requires a port it When running a
  python process that requires a port it
long_description: When running a python process that requires a port it When running
  a python process that requires a port it
now: 2022-05-07 21:32:25.892744
path: pages/blog/python-find-available-port.md
slug: python-find-available-port
status: published
super_description: When running a python process that requires a port it When running
  a python process that requires a port it
tags:
- python
templateKey: til
title: Python Find Available Port
today: 2022-05-07
year: 2022
---

When running a python process that requires a port it's handy if there is an
option for it to just run on the next avaialble port.  To do this we can use
the socket module to determine if the port is in use or not before starting our
process.

``` python
import socket

def find_port(port=8000):
    """Find a port not in ues starting at given port"""
    with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
        if s.connect_ex(("localhost", port)) == 0:
            return find_port(port=port + 1)
        else:
            return port
```