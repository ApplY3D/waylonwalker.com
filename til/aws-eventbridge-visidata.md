---
content: ''
cover: ''
date: 2022-02-15
datetime: 2022-02-15 00:00:00+00:00
description: Reading eventbridge rules from the command line can be a total drag,
  pipe it Reading eventbridge rules from the command line can be a total drag, pipe
  it I just
long_description: Reading eventbridge rules from the command line can be a total drag,
  pipe it Reading eventbridge rules from the command line can be a total drag, pipe
  it I just love when I start thinking through how to parse a bunch of json at the
  I just love when I
now: 2022-05-07 21:32:25.891643
path: pages/til/aws-eventbridge-visidata.md
slug: til/aws-eventbridge-visidata
status: published
super_description: Reading eventbridge rules from the command line can be a total
  drag, pipe it Reading eventbridge rules from the command line can be a total drag,
  pipe it I just love when I start thinking through how to parse a bunch of json at
  the I just love when I start thinking through how to parse a bunch of json at the
tags:
- python
- cli
- bash
templateKey: til
title: View AWS event bridge rules with visidata
today: 2022-05-07
year: 2022
---

Reading eventbridge rules from the command line can be a total drag, pipe it
into visidata to make it a breeze.

I just love when I start thinking through how to parse a bunch of json at the
command line, maybe building out my own custom cli, then the solution is as
simple as piping it into visidata.  Which is a fantastic tui application that
had a ton of vim-like keybindings and data features.


``` python
alias awsevents = aws events list-rules | visidata -f json
```