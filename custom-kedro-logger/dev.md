---
canonical_url: https://waylonwalker.com/custom-kedro-logger/
cover_image: https://images.waylonwalker.com/custom-kedro-logger.png
description: DRAFT - DRAFT -
published: true
tags:
- kedro
- python
title: Custom Kedro Logger
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