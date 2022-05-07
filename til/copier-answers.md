---
content: ''
cover: ''
date: 2022-01-08
datetime: 2022-01-08 00:00:00+00:00
description: 'The copier answers file is a key component to making your templates
  The copier answers file is a key component to making your templates Inside of my  Inside
  of '
long_description: The copier answers file is a key component to making your templates
  The copier answers file is a key component to making your templates Inside of my  Inside
  of my  Inside my copier.yml I have setup my  Inside my copier.yml I have setup my  Once
  I cha
now: 2022-05-07 21:32:25.891697
path: pages/til/copier-answers.md
slug: til/copier-answers
status: published
super_description: The copier answers file is a key component to making your templates
  The copier answers file is a key component to making your templates Inside of my  Inside
  of my  Inside my copier.yml I have setup my  Inside my copier.yml I have setup my  Once
  I change the  Once I change the  I I After rendering the template we have the following
  content in our After rendering the template we have the following content in our
  This is where I was most stuck, primarily becuase  This is where I was most stuck,
  pri
tags:
- python
- linux
- cli
templateKey: til
title: Using Copier Answers to rerun templates quickly
today: 2022-05-07
year: 2022
---

The copier answers file is a key component to making your templates
re-runnable.  Let's look at the example for my setup.py.

``` bash
❯ tree ~/.copier-templates/setup.py
/home/walkers/.copier-templates/setup.py
├── [[ _copier_conf.answers_file ]].tmpl
├── copier.yml
├── setup.cfg
└── setup.py.tmpl

0 directories, 4 files
```

Inside of my `[[ _copier_conf.answers_file ]].tmpl` file is this, a
message not to muck around with it, and the ansers in yaml form.  The
first line is just a helper for the blog post.

``` yaml
# ~/.copier-templates/setup.py/\[\[\ _copier_conf.answers_file\ \]\].tmpl
# Changes here will be overwritten by Copier; NEVER EDIT MANUALLY
[[_copier_answers|to_nice_yaml]]
```

Inside my copier.yml I have setup my _answers_file to point to a special
file.  This is because this is not a whole projet template, but one just
for a single file.

``` yaml
# copier.yml
# ...
_answers_file: .setup-py-copier-answers.yml
```

> Once I change the _answers_file I was incredibly stuck

## Run it

I'm making a library of personal copier templates in my
`~/.copier-templates` directory and I am going to run it from there.

``` bash
copier copy ~/.copier-templates/setup.py
```
## Results

After rendering the template we have the following content in our
`.setup.setup-py-copier-answers.yml` file.  This will allow us to update
quick if we ever change our template.

``` yaml
# .setup-py-copier-answers.yml
# Changes here will be overwritten by Copier; NEVER EDIT MANUALLY
_src_path: /home/walkers/.copier-templates/setup.py
author_github: waylonwalker
author_name: Waylon Walker
description: awesomeness
framework: null
keywords: null
package_name: my-package
```

## Update it

This is where I was most stuck, primarily becuase `-a <answers_file>`
must come exactly after the base command `copier`.  This felt a bit odd
to and not where I expected it so it.

``` bash
copier -a .setup-py-copier-answers.yml update
```

## Stop asking all these damn questions

So the defaults are now changed to our previous results, but it keeps
asking for them.  To stop asking we can simply add a `-f` flag.

``` bash
copier -fa .setup-py-copier-answers.yml update
```