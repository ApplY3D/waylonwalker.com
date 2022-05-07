---
canonical_url: https://waylonwalker.com/til/gpg-sign-git-ssh/
cover_image: https://images.waylonwalker.com/til/gpg-sign-git-ssh.png
description: 'I was editing some blog posts over ssh, when I ran into I was editing
  some blog posts over ssh, when I ran into This is the error message I was seeing.
  This is '
published: true
tags:
- git
title: GPG signing commits over ssh
---

I was editing some blog posts over ssh, when I ran into this error.  gpg was failing to sign my commits.  I realized that this was because I could not answer to the desktop keyring over ssh, but had no idea how to fix it.

## Error

This is the error message I was seeing.

```
gpg failed to sign the data ssh
```

## The fix

The fix ended up being pretty simple, but quite a ways down this [stack overflow post](https://stackoverflow.com/questions/41052538/git-error-gpg-failed-to-sign-data/41054093). This environment variable tells gpg that we are not logged into a desktop and it does not try to use the desktop keyring, and asks to unlog the gpgkey right in the terminal.

``` bash
export GPG_TTY=$(tty)
```

## The log in menu

This is what it looks like when it asks for the passphrase.

![enter your passphrase to unlock your gpg key](https://images.waylonwalker.com/gpg-passphrase-unlock.png)