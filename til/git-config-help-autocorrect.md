---
content: ''
cover: ''
date: 2022-03-15
datetime: 2022-03-15 00:00:00+00:00
description: If you have ever mistyped a git command very close to an existing one
  If you have ever mistyped a git command very close to an existing one What you might
  not h
long_description: 'If you have ever mistyped a git command very close to an existing
  one If you have ever mistyped a git command very close to an existing one What you
  might not have known is that you can configure git to just run What you might not
  have known is that '
now: 2022-05-07 21:32:25.891506
path: pages/til/git-config-help-autocorrect.md
slug: til/git-config-help-autocorrect
status: published
super_description: If you have ever mistyped a git command very close to an existing
  one If you have ever mistyped a git command very close to an existing one What you
  might not have known is that you can configure git to just run What you might not
  have known is that you can configure git to just run Now when you typo a git command
  it will autmatically run after the Now when you typo a git command it will autmatically
  run after the I I
tags:
- git
- cli
templateKey: til
title: Configure Git to Autocorrect Your Fat Fingers
today: 2022-05-07
year: 2022
---

If you have ever mistyped a git command very close to an existing one
you have likely seen this message.

``` bash
❯ git chekout dev
git: 'chekout' is not a git command. See 'git --help'.

The most similar command is
        checkout
```

## Automatically run the right one

What you might not have known is that you can configure git to just run
this command for you.

``` bash
# Gives you 0.1 seconds to respond
git config --global help.autocorrect 1

# Gives you 1 seconds to respond
git config --global help.autocorrect 10

# Gives you 5 seconds to respond
git config --global help.autocorrect 50
```

## Fat Fingers Gone

Now when you typo a git command it will autmatically run after the
configured number of tenths of a second.

``` bash
❯ git chkout get-error
WARNING: You called a Git command named 'chkout', which does not exist.
Continuing in 1.0 seconds, assuming that you meant 'checkout'.
M       pages/blog/how-i-deploy-2021.md
M       pages/hot_tips/001.md
M       pages/templates/gratitude_card.html
M       plugins/index.py
M       plugins/publish_amp.py
M       plugins/render_template_variables.py
M       plugins/youtube.py
M       requirements.txt
M       static/index.html
Switched to branch 'get-error'
```

## My config

I'm rocking 10 for now just to see how I feel about it, but honestly I
cannot think of a time that I have seen the original warning that was
not what I wanted.  This at least gives me some time to respond if I am
unsure.

``` bash
git config --global help.autocorrect 10
```