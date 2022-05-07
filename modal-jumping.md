---
content: ''
cover: ''
date: 2021-06-03
datetime: 2021-06-03 00:00:00+00:00
description: ''
long_description: ''
now: 2022-05-07 21:32:25.892934
path: pages/blog/modal-jumping.md
slug: modal-jumping
status: draft
super_description: ''
tags:
- vim
templateKey: blog-post
title: Modal jumping
today: 2022-05-07
year: 2021
---

```
nnoremap <leader>e :execute getline(".")<cr>j
```

```
nnoremap <c-j> g,
nnoremap <c-k> g;
```

```
nnoremap <c-j> <c-]>
nnoremap <c-k> g;
```

```
nnoremap <c-j> :cnext<cr>
nnoremap <c-k> :cprev<cr>
```

```
nnoremap <c-j> :lnext<cr>
nnoremap <c-k> :lprev<cr>
```

```
nnoremap <c-j> :tnext<cr>
nnoremap <c-k> :tprevious<cr>
nnoremap <c-j> :trewind<cr>
nnoremap <c-k> :tprevious<cr>
```