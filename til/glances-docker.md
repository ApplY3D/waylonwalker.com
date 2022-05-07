---
content: ''
cover: ''
date: 2022-02-22
datetime: 2022-02-22 00:00:00+00:00
description: 'Glances is a system monitor with a ton of features, including docker
  processes. Glances is a system monitor with a ton of features, including docker
  processes. '
long_description: Glances is a system monitor with a ton of features, including docker
  processes. Glances is a system monitor with a ton of features, including docker
  processes. I have started using portainer to look at running docker processes, its
  a great I have sta
now: 2022-05-07 21:32:25.892206
path: pages/til/glances-docker.md
slug: til/glances-docker
status: published
super_description: Glances is a system monitor with a ton of features, including docker
  processes. Glances is a system monitor with a ton of features, including docker
  processes. I have started using portainer to look at running docker processes, its
  a great I have started using portainer to look at running docker processes, its
  a great You will need to install glances to use the glances webui.  We can still
  use You will need to install glances to use the glances webui.  We can still use
  You will be presented with
tags:
- python
templateKey: til
title: Glances can watch docker processes
today: 2022-05-07
year: 2022
---

Glances is a system monitor with a ton of features, including docker processes.

I have started using portainer to look at running docker processes, its a great
heavy-weight docker process monitor.  glances works as a great lightweight
monitor to just give you the essentials, ( Name, Status, CPU%, MEM, /MAX,
IOR/s, IOW/s, Rx/s, Tx/s, Command)

## install

You will need to install glances to use the glances webui.  We can still use
`pipx` to manage our virtual environment for us so that we do not need to do so
manually or run the risk of globally installed package dependency hell.

``` bash
pipx install glances
pipx inject glances "glances[docker]"
```

You will be presented with this success message.

``` bash
  injected package glances into venv glances
done! ✨ 🌟 ✨
```

## results

Now running glances will also show information about your running docker
containers.

![running glances with docker installed will show your docker processes](https://images.waylonwalker.com/glances-docker.png)


## Links

* [glances docker](https://glances.readthedocs.io/en/catest/docker.html)
* [pipx](https://pypa.github.io/pipx/)
* [website](https://nicolargo.github.io/glances/)
* [docs](https://glances.readthedocs.io/en/latest/index.html)
* [github](https://github.com/nicolargo/glances)