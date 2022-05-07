---
content: ''
cover: ''
date: 2021-01-20
datetime: 2021-01-20 00:00:00+00:00
description: This is a post that may be a work in progress for awhile, Its a collections
  of This is a post that may be a work in progress for awhile, Its a collections of
  po
long_description: This is a post that may be a work in progress for awhile, Its a
  collections of This is a post that may be a work in progress for awhile, Its a collections
  of posts posts tags tags draft posts draft posts frontmatter frontmatter filepath
  filepath cont
now: 2022-05-07 21:32:25.892606
path: pages/blog/markdown-cli.md
slug: markdown-cli
status: published
super_description: This is a post that may be a work in progress for awhile, Its a
  collections of This is a post that may be a work in progress for awhile, Its a collections
  of posts posts tags tags draft posts draft posts frontmatter frontmatter filepath
  filepath content content template template html html Markdown.Markdown Markdown.Markdown
  support extentsions support extentsions provide ways to hook in or clean up the
  frontmatter provide ways to hook in or clean up the frontmatter load load render
  render save s
tags:
- python
- blog
templateKey: blog-post
title: Markdown Cli
today: 2022-05-07
year: 2021
---

This is a post that may be a work in progress for awhile, Its a collections of
thoughts on managing my blog, but could be translated into anythiung that is
just a collection of markdown.

## Listing things

* posts
* tags
* draft posts

## data

* frontmatter
* filepath
* content
* template
* html

## render content

* Markdown.Markdown
* support extentsions

## frontmatter cleaning.

* provide ways to hook in or clean up the frontmatter

## Markata.Markata methods

* load
* render
* save

## Markata.Post methods

* load
* render
* save

## Markata plugins

* before_load
* before_post_load
* after_load
* after_post_load
* before_save
* before_post_save
* after_save
* after_post_save


## Markata plugins

* cleanse_frontmatter
* html_feed
* json_feed
* rss_feed
* save_posts




## CLI

``` bash
$ markata list tags

python
data
```

``` bash
$ markata

[
  { 
    "title": "post title",
    "description": "this is a post",
    "filepath": "path_to.md",
    "content": "the content of the post",
    "html": "<p>the content of the post</p>"
    },
    ...
]
```

``` bash
```