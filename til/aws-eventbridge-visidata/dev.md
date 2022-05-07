---
canonical_url: https://waylonwalker.com/til/aws-eventbridge-visidata/
cover_image: https://images.waylonwalker.com/til/aws-eventbridge-visidata.png
description: Reading eventbridge rules from the command line can be a total drag,
  pipe it Reading eventbridge rules from the command line can be a total drag, pipe
  it I just
published: true
tags:
- python
- cli
- bash
title: View AWS event bridge rules with visidata
---

Reading eventbridge rules from the command line can be a total drag, pipe it into visidata to make it a breeze.

I just love when I start thinking through how to parse a bunch of json at the command line, maybe building out my own custom cli, then the solution is as simple as piping it into visidata.  Which is a fantastic tui application that had a ton of vim-like keybindings and data features.


``` python
alias awsevents = aws events list-rules | visidata -f json
```