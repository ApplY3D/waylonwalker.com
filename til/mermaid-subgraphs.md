---
content: ''
cover: ''
date: 2022-03-05
datetime: 2022-03-05 00:00:00+00:00
description: Mermaid provides some really great ways to group or fence in parts of
  your Mermaid provides some really great ways to group or fence in parts of your
  Here we ca
long_description: Mermaid provides some really great ways to group or fence in parts
  of your Mermaid provides some really great ways to group or fence in parts of your
  Here we can model some sort of data ingest with some raw iot device and our Here
  we can model some s
now: 2022-05-07 21:32:25.891711
path: pages/til/mermaid-subgraphs.md
slug: til/mermaid-subgraphs
status: published
super_description: Mermaid provides some really great ways to group or fence in parts
  of your Mermaid provides some really great ways to group or fence in parts of your
  Here we can model some sort of data ingest with some raw iot device and our Here
  we can model some sort of data ingest with some raw iot device and our If we want
  to connect them, we can make a connection between a and A outside of If we want
  to connect them, we can make a connection between a and A outside of It It
tags:
- webdev
templateKey: til
title: Grouping Mermaid nodes in Subgraphs
today: 2022-05-07
year: 2022
---

Mermaid provides some really great ways to group or fence in parts of your
graphs through the use of subgraphs.

Here we can model some sort of data ingest with some raw iot device and our
warehouse in different groups.

```
graph TD;

    subgraph raw_iot
        a
    end

    subgraph warehouse
        A --> B
        B --> C
    end
```
<script src='https://unpkg.com/mermaid@8.1.0/dist/mermaid.min.js'></script>
<div class='mermaid'>
graph TD;

    subgraph raw_iot
        a
    end

    subgraph warehouse
        A --> B
        B --> C
    end
</div>

## connecting subgroups

If we want to connect them, we can make a connection between a and A outside of
the subgraphs.

```
graph TD;

    subgraph raw_iot
        a
    end

    a --> A

    subgraph warehouse
        A --> B
        B --> C
    end
```
<script src='https://unpkg.com/mermaid@8.1.0/dist/mermaid.min.js'></script>
<div class='mermaid'>
graph TD;

    subgraph raw_iot
        a
    end

    a --> A

    subgraph warehouse
        A --> B
        B --> C
    end
</div>

## separation of concerns

It's also possible to specify subgraphs separate from where you define your
nodes. which allows for some different levels of grouping that would not be
possible if you were to define all your nodes inside of a subgraph.

```
graph TD;
    a --> A
    A --> B
    B --> C

    subgraph one
        A
        C
    end
```


<div class='mermaid'>
graph TD;
    a --> A
    A --> B
    B --> C

    subgraph warehouse
        A
        C
    end
</div>