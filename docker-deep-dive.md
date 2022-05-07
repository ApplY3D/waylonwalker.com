---
content: ''
cover: ''
date: 2021-04-23
datetime: 2021-04-23 00:00:00+00:00
description: https://www.hanselminutes.com/784/doing-open-source-with-brian-douglas
  https://www.hanselminutes.com/784/doing-open-source-with-brian-douglas A handy way
  to try
long_description: https://www.hanselminutes.com/784/doing-open-source-with-brian-douglas
  https://www.hanselminutes.com/784/doing-open-source-with-brian-douglas A handy way
  to try weird things in docker is using A handy way to try weird things in docker
  is using Instal
now: 2022-05-07 21:32:25.892805
path: pages/blog/docker-deep-dive.md
slug: docker-deep-dive
status: draft
super_description: https://www.hanselminutes.com/784/doing-open-source-with-brian-douglas
  https://www.hanselminutes.com/784/doing-open-source-with-brian-douglas A handy way
  to try weird things in docker is using A handy way to try weird things in docker
  is using Installing on Ubuntu. Installing on Ubuntu. In order to run docker commands
  without using sudo you need to add docker to In order to run docker commands without
  using sudo you need to add docker to Namespaces and Control Groups are hard, which
  is why conta
tags:
- docker
- linux
templateKey: blog-post
title: "\U0001F4DD Docker Deep Dive - Notes"
today: 2022-05-07
year: 2021
---

https://www.hanselminutes.com/784/doing-open-source-with-brian-douglas

## Play With Docker

A handy way to try weird things in docker is using
[play-with-docker](play-with-docker.com).  You get a four hour session for
free, after four hours everything will be deleted, but you can start a new
session.

### Installing Docker on Linux

Installing on Ubuntu.

``` bash
wget -qO- https://get.docker.com/ | sh
```

### Running Docker commands without sudo

In order to run docker commands without using sudo you need to add docker to
your group.


``` bash
sudo usermod -aG docker ubuntu
```

## Architecture and Theory


**Container** - Isolated area of an OS with resource usage limits applied.

Namespaces and Control Groups are hard, which is why containers were unusable
by mortals before docker.



## Namespaces
_Isolation_

Each container looks and feels like a regular OS. It has its own eth0, users,
kernel.  These are completely isolated from every other container running on
the system.

Namespaces are analogous to what Hypervisors do on hardware.

* Process ID (pid)
* Network (net)
* Filesystem/mount (mnt)
* Inter-proc comms (ipc)
* UTS (uts)
* User (usr)

##  Control Groups
_Resource usage limits_