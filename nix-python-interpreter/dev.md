---
canonical_url: https://waylonwalker.com/nix-python-interpreter/
cover_image: https://images.waylonwalker.com/nix-python-interpreter.png
description: I recently started playing with nix. I recently started playing with
  nix. automatically select correct python version per project automatically select
  correct p
published: true
tags:
- python
title: Using Nix to manage my Python Interpreter
---

I recently started playing with nix.

## goals

* automatically select correct python version per project
* activating one doesn't bleed into the other



## Installing nix

``` bash
curl -L https://nixos.org/nix/install | sh
```

## controlling nix-env

``` bash
nix-env -iA nixpkgs.python310 nix-env -iA nixpkgs.python39 nix-env -iA nixpkgs.python38 nix-env -iA nixpkgs.python37
```

## searching for packages

https://search.nixos.org/

```
nix-env -qaP .\*python.\*
```

``` bash
nix search nixpkgs python
```

## shell

```
nix-shell -p python39
```