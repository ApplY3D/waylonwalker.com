---
canonical_url: https://waylonwalker.com/python-find-available-port/
cover_image: https://images.waylonwalker.com/python-find-available-port.png
description: When running a python process that requires a port it When running a
  python process that requires a port it
published: true
tags:
- python
title: Python Find Available Port
---

When running a python process that requires a port it's handy if there is an option for it to just run on the next avaialble port.  To do this we can use the socket module to determine if the port is in use or not before starting our process.

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