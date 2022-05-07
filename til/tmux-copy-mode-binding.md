---
content: ''
cover: ''
date: 2022-02-13
datetime: 2022-02-13 00:00:00+00:00
description: The default keybinding for copy-mode  The default keybinding for copy-mode  To
  do this I just popped open my  To do this I just popped open my  I have a full vi
long_description: The default keybinding for copy-mode  The default keybinding for
  copy-mode  To do this I just popped open my  To do this I just popped open my  I
  have a full video on copy-mode you can find here. I have a full video on copy-mode
  you can find here. ht
now: 2022-05-07 21:32:25.891477
path: pages/til/tmux-copy-mode-binding.md
slug: til/tmux-copy-mode-binding
status: published
super_description: The default keybinding for copy-mode  The default keybinding for
  copy-mode  To do this I just popped open my  To do this I just popped open my  I
  have a full video on copy-mode you can find here. I have a full video on copy-mode
  you can find here. https://waylonwalker.com/tmux-copy-mode/ https://waylonwalker.com/tmux-copy-mode/
tags:
- tmux
- cli
templateKey: til
title: A better copy-mode bind for Tmux
today: 2022-05-07
year: 2022
---

The default keybinding for copy-mode `<prefix>-[` is one that is just so
awkward for me to hit that I end up not using it at all.  I was on a
call with my buddy Nic this week and saw him just fluidly jump into
`copy-mode` in an effortless fashion, so I had to ask him for his
keybinding and it just made sense. Enter, that's it.  So I have addedt
his to my `~/.tmux.conf` along with one for `alt-enter` and have found
myself using it way more so far.

## Setting copy-mode to enter

To do this I just popped open my `~/.tmux.conf` and added the following.
Now I can get to `copy-mode` with `<prefix>-Enter` which is `control-b
Enter`, or `alt-enter`.

```bash
bind Enter copy-mode
bind -n M-Enter copy-mode
```

## More on copy-mode

I have a full video on copy-mode you can find here.


  <div class="onelinelink-wrapper">
      <a class="onelinelink" href="https://waylonwalker.com/tmux-copy-mode/">
          <img style="float: right;" align='right' src="https://images.waylonwalker.com/tmux-copy-mode-og_250x140.png" alt="article cover for 
 tmux copy-mode
"/>
          <p><strong>
 tmux copy-mode
</strong></p>
      </a>
  </div>