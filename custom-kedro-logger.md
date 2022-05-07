---
content: ''
cover: ''
date: 2021-05-02
datetime: 2021-05-02 00:00:00+00:00
description: DRAFT - DRAFT -
long_description: DRAFT - DRAFT -
now: 2022-05-07 21:32:25.894282
path: pages/blog/custom-kedro-logger.md
slug: custom-kedro-logger
status: draft
super_description: DRAFT - DRAFT -
tags:
- kedro
- python
templateKey: blog-post
title: Custom Kedro Logger
today: 2022-05-07
year: 2021
---

DRAFT - 



``` yaml
formatters:
    mine:
        format: "%(asctime)s - %(name)s - %(levelname)s - %(message)s - %(me)s"

handlers:

    mine_handler:
        class: logging.StreamHandler
        level: INFO
        formatter: mine
        stream: ext://sys.stdout

loggers:
    me:
        level: DEBUG
        handlers: [mine_handler]

root:
    level: INFO
    handlers: [console, info_file_handler, error_file_handler]
```