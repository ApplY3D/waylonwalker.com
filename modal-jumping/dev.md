---
canonical_url: https://waylonwalker.com/modal-jumping/
cover_image: https://images.waylonwalker.com/modal-jumping.png
description: ''
published: true
tags:
- vim
title: Modal jumping
---

```
nnoremap <leader>e :execute getline(".")<cr>j
```

```
nnoremap <c-j> g, nnoremap <c-k> g;
```

```
nnoremap <c-j> <c-]> nnoremap <c-k> g;
```

```
nnoremap <c-j> :cnext<cr> nnoremap <c-k> :cprev<cr>
```

```
nnoremap <c-j> :lnext<cr> nnoremap <c-k> :lprev<cr>
```

```
nnoremap <c-j> :tnext<cr> nnoremap <c-k> :tprevious<cr> nnoremap <c-j> :trewind<cr> nnoremap <c-k> :tprevious<cr>
```