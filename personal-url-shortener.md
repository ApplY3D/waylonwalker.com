---
content: ''
cover: ''
date: 2020-01-29
datetime: 2020-01-29 00:00:00+00:00
description: Personal URL shortener with Netlify Redirects
long_description: I love using URL shorteners to easily share links without hitting
  character I love using URL shorteners to easily share links without hitting character
  I recently discovered a really cool feature of netlify that I have always looked
  past,  I recently
now: 2022-05-07 21:32:25.892751
path: pages/blog/personal-url-shortener.md
slug: personal-url-shortener
status: published
super_description: I love using URL shorteners to easily share links without hitting
  character I love using URL shorteners to easily share links without hitting character
  I recently discovered a really cool feature of netlify that I have always looked
  past,  I recently discovered a really cool feature of netlify that I have always
  looked past,  simply add a  simply add a  Now with shorter links we have more space
  for our content without needing to use a service like bit.ly that makes our links
  unreadable. Now with
tags:
- webdev
- blog
templateKey: blog-post
title: Personal URL shortener with Netlify Redirects
today: 2022-05-07
year: 2020
---

I love using URL shorteners to easily share links without hitting character
limits, but they loose their meaning. Services like bit.ly will save my links
for me so that I can find them, but I would rather them to be easy to remember.
[https://bit.ly/2ruLwQz](https://bit.ly/2ruLwQz "https://bit.ly/2ruLwQz") does
not roll of the tongue so well.

## 301 🤸‍♀️

I recently discovered a really cool feature of netlify that I have always looked past, `_redirects`. It is so simple cool and powerful, every netlify site should do this!

## But how 🤷‍♀️

simply add a `_redirects` file to the root of your your published site with the following format. The trick I found with my gatsby site was that it needed to be in my static directory `/static/_redirects`, not root. Next you just put space separated links on separate lines. #'s can be used for comments.

``` markdown
# netlify redirects
# from_url to_url

# Short-Blog

/blog/scli         /blog/simple-click/
/blog/cmdt         /blog/cmd-exe-tips/
.
.
.


# splats

/b*             /blog/:splat
/n*             /notes/:splat


# External

/twitter        https://twitter.com/_WaylonWalker
/github         https://github.com/WaylonWalker
/devto          https://dev.to/waylonwalker/
```

## 🙌 Share those short links

Now with shorter links we have more space for our content without needing to use a service like bit.ly that makes our links unreadable.

![url shortener](https://images.waylonwalker.com/URL shortener.png)