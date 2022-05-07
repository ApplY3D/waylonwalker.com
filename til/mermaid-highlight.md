---
content: ''
cover: ''
date: 2022-03-07
datetime: 2022-03-07 00:00:00+00:00
description: Mermaid gives us a way to style nodes through the use of css, but rather
  than Mermaid gives us a way to style nodes through the use of css, but rather than
  prod
long_description: Mermaid gives us a way to style nodes through the use of css, but
  rather than Mermaid gives us a way to style nodes through the use of css, but rather
  than produces the following graph produces the following graph style one fill:#BADA55
  style one fil
now: 2022-05-07 21:32:25.891619
path: pages/til/mermaid-highlight.md
slug: til/mermaid-highlight
status: published
super_description: Mermaid gives us a way to style nodes through the use of css, but
  rather than Mermaid gives us a way to style nodes through the use of css, but rather
  than produces the following graph produces the following graph style one fill:#BADA55
  style one fill:#BADA55
tags:
- webdev
templateKey: til
title: Mermaid Highlight
today: 2022-05-07
year: 2022
---

Mermaid gives us a way to style nodes through the use of css, but rather than
using normal css selectors we need to use `style <nodeid>`.  This also applies
to subgraphs, and we can use the name of the subgraph in place of the nodeid.

``` ruby
graph TD;
    a --> A
    A --> B
    B --> C

    style A fill:#f9f,stroke:#333,stroke-width:4px
    style B fill:#f9f,stroke:#333,stroke-width:4px

    subgraph one
        a
    end

    style one fill:#BADA55
```

produces the following graph

<script src='https://unpkg.com/mermaid@8.1.0/dist/mermaid.min.js'></script>
<div class='mermaid'>
graph TD;
a --> A
A --> B
B --> C
style A fill:#f9f,stroke:#333,stroke-width:4px
style B fill:#f9f,stroke:#333,stroke-width:4px
subgraph one
  a
end

style one fill:#BADA55
</div>