---
content: ''
cover: ''
date: 2022-02-24
datetime: 2022-02-24 00:00:00+00:00
description: Mermaid diagrams provide a way to display graphs defined as plain text.
  Mermaid diagrams provide a way to display graphs defined as plain text. You can
  define n
long_description: Mermaid diagrams provide a way to display graphs defined as plain
  text. Mermaid diagrams provide a way to display graphs defined as plain text. You
  can define nodes like this in mermaid, and GitHub will now render You can define
  nodes like this in me
now: 2022-05-07 21:32:25.891957
path: pages/til/github-supports-mermaid.md
slug: til/github-supports-mermaid
status: published
super_description: Mermaid diagrams provide a way to display graphs defined as plain
  text. Mermaid diagrams provide a way to display graphs defined as plain text. You
  can define nodes like this in mermaid, and GitHub will now render You can define
  nodes like this in mermaid, and GitHub will now render
tags:
- python
- python
- python
templateKey: til
title: GitHub Markdown now Supports Mermaid Diagrams
today: 2022-05-07
year: 2022
---

Mermaid diagrams provide a way to display graphs defined as plain text.
Some markdown renderers support this as a plugin.  GitHub now supports
it.

## example

You can define nodes like this in mermaid, and GitHub will now render
them as a pretty graph diagram.  Its rendered in svg, so its searchable
with `control f` and everything.

```mermaid
  graph TD;
      A-->B;
      A-->C;
      B-->D;
      C-->D-->OUT;
      E-->F-->G-->OUT
```

![Here is what the example looks like on
GitHub](https://images.waylonwalker.com/example-gh-mermaid.png)

## Links

* [GitHub support announcement](https://github.blog/2022-02-14-include-diagrams-markdown-files-mermaid/)
* [mermaid docs](https://mermaid-js.github.io/mermaid/#/)