---
content: ''
cover: ''
date: 2022-01-07
datetime: 2022-01-07 00:00:00+00:00
description: 'Once you have made your sick looking cli apps with rich, eventually
  you are Once you have made your sick looking cli apps with rich, eventually you
  are Install '
long_description: Once you have made your sick looking cli apps with rich, eventually
  you are Once you have made your sick looking cli apps with rich, eventually you
  are Install them from the command line. Install them from the command line. Import
  make a .py file and
now: 2022-05-07 21:32:25.892144
path: pages/til/simple-textual-widget.md
slug: til/simple-textual-widget
status: published
super_description: Once you have made your sick looking cli apps with rich, eventually
  you are Once you have made your sick looking cli apps with rich, eventually you
  are Install them from the command line. Install them from the command line. Import
  make a .py file and import them in it. Import make a .py file and import them in
  it. If you return your rich renderable out of class that inherits from If you return
  your rich renderable out of class that inherits from You You At this point It probably
  does not look mu
tags:
- python
- cli
templateKey: til
title: Making a Textual Widget from a Rich Renderable
today: 2022-05-07
year: 2022
---

Once you have made your sick looking cli apps with rich, eventually you are
going to want to add some keybindings to them.  Currently Textual, also written
by [@willmcgugan](https://twitter.com/willmcgugan), does this extremely well.
Fair Warning it is in super beta mode and expected to change a bunch.  So take
it easy with hopping on the train so fast.

## Get the things


Install them from the command line.

``` bash
pip install textual
pip install rich
```

Import make a .py file and import them in it.

``` python
from textual.app import App
from textual.widget import Widget
from rich.panel import Panel
```

## Make what you have a widget

If you return your rich renderable out of class that inherits from
`textual.widget.Widget`, you can then dock this inside of an app class
inheriting from `textual.app.App`.

``` python
class MyWidget(Widget):
    def render(self):
        my_renderable = Panel("press q to quit")
        return my_renderable

class MyApp(App):
    async def on_mount(self) -> None:
        await self.view.dock(MyWidget(), edge="top")
        await self.bind("q", "quit")
```

## run it

You've made a TUI (text user interface).  Run the classmethod `run` to display
the it in its full screen glory.

``` python
MyApp.run(log="textual.log")
```

## Final result

At this point It probably does not look much different, but it can be
interactive by binding keys to any method on your app that starts with the word
`action_`, this includes the built-in actions such as `action_quit`.

``` python
from textual.app import App
from textual.widget import Widget
from rich.panel import Panel


class MyWidget(Widget):
    def render(self):
        my_renderable = Panel("press q to quit")
        return my_renderable


class MyApp(App):
    async def on_mount(self) -> None:
        await self.view.dock(MyWidget(), edge="top")
        await self.bind("q", "quit")


if __name__ == "__main__":
    MyApp.run(log="textual.log")
```