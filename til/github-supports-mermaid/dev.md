---
canonical_url: https://waylonwalker.com/til/github-supports-mermaid/
cover_image: https://images.waylonwalker.com/til/github-supports-mermaid.png
description: Mermaid diagrams provide a way to display graphs defined as plain text.
  Mermaid diagrams provide a way to display graphs defined as plain text. You can
  define n
published: true
tags:
- python
- python
- python
title: GitHub Markdown now Supports Mermaid Diagrams
---

Mermaid diagrams provide a way to display graphs defined as plain text. Some markdown renderers support this as a plugin.  GitHub now supports it.

## example

You can define nodes like this in mermaid, and GitHub will now render them as a pretty graph diagram.  Its rendered in svg, so its searchable with `control f` and everything.

```mermaid
  graph TD;
      A-->B;
      A-->C;
      B-->D;
      C-->D-->OUT;
      E-->F-->G-->OUT
```

![Here is what the example looks like on GitHub](https://images.waylonwalker.com/example-gh-mermaid.png)

## Links

* [GitHub support announcement](https://github.blog/2022-02-14-include-diagrams-markdown-files-mermaid/)
* [mermaid docs](https://mermaid-js.github.io/mermaid/#/)