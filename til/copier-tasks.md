---
content: ''
cover: ''
date: 2022-01-22
datetime: 2022-01-22 00:00:00+00:00
description: 'Copier allows you to run post render tasks, just like cookiecutter.
  These are Copier allows you to run post render tasks, just like cookiecutter. These
  are The '
long_description: 'Copier allows you to run post render tasks, just like cookiecutter.
  These are Copier allows you to run post render tasks, just like cookiecutter. These
  are The example I have below runs an  The example I have below runs an  I have put
  the script in  '
now: 2022-05-07 21:32:25.892185
path: pages/til/copier-tasks.md
slug: til/copier-tasks
status: published
super_description: 'Copier allows you to run post render tasks, just like cookiecutter.
  These are Copier allows you to run post render tasks, just like cookiecutter. These
  are The example I have below runs an  The example I have below runs an  I have put
  the script in  I have put the script in '
tags:
- python
- cli
- linux
templateKey: til
title: Copier Tasks | Python templating post run task
today: 2022-05-07
year: 2022
---

Copier allows you to run post render tasks, just like cookiecutter. These are
defined as a list of `tasks` in your `copier.yml`.  They are simply shell
commands to run.

The example I have below runs an `update-gratitude` bash script after the
copier template has been rendered.

``` yaml
# copier.yml
num: 128
_answers_file: .gratitude-copier-answers.yml
_tasks:
  - "update-gratitude"
```

I have put the script in `~/.local/bin` so that I know it's always on my
`$PATH`.  It will reach back into the `copier.yml` and update the default
number.


``` bash
#!/bin/bash
# ~/.local/bin/update-gratitude
current=`awk '{print $2}' ~/.copier-templates/gratitude/copier.yml | head -n 1`
new=`expr $current + 1`
echo $current
echo $new
sed -i "s/$current/$new/g" ~/.copier-templates/gratitude/copier.yml
```