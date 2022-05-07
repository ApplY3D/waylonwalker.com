---
content: ''
cover: ''
date: 2022-03-09
datetime: 2022-03-09 00:00:00+00:00
description: Has no upstream branch errors in git can be such a damn productivity
  killer. Has no upstream branch errors in git can be such a damn productivity killer.
  If you
long_description: Has no upstream branch errors in git can be such a damn productivity
  killer. Has no upstream branch errors in git can be such a damn productivity killer.
  If you have not yet configured git to always push to the current branch, you If
  you have not yet
now: 2022-05-07 21:32:25.892137
path: pages/til/git-push-default-current.md
slug: til/git-push-default-current
status: published
super_description: Has no upstream branch errors in git can be such a damn productivity
  killer. Has no upstream branch errors in git can be such a damn productivity killer.
  If you have not yet configured git to always push to the current branch, you If
  you have not yet configured git to always push to the current branch, you Let Let
  You will be presented with the following error. You will be presented with the following
  error. To resolve this fatal error your first option is simply to follow the To
  resolve this fa
tags:
- git
templateKey: til
title: Configure Git to Always Push to the Current Branch
today: 2022-05-07
year: 2022
---

Has no upstream branch errors in git can be such a damn productivity killer.
You gotta stop your flow and swap over the branch, there is a config so that
you don't have to do this.

## **fatal** has no upstream branch

If you have not yet configured git to always push to the current branch, you
will get a `has no upstream branch` error if you don't explicitly set it.

Let's show an example

``` bash
git checkout -b feat/ingest-inventory-data
git add conf/base/catalog.yml
git commit -m "feat: ingest inventory data from abc-db"
git push
```

You will be presented with the following error.

``` bash
fatal: The current branch feat/ingest-inventory-data has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin feat/ingest-inventory-data
```
## Option 1: follow the instructions

To resolve this fatal error your first option is simply to follow the
instructions given.  Just copy and paste it in.

``` bash
git push --set-upstream origin feat/ingest-inventory-data
```

## Option 2: push to current bransh wihtout setting upstream

Honestly I am pretty aware of the branch I am on, and Very few times have I
ever accidently pushed to the wrong branch.  The one that you might have a
bigger chance with a more detrimental effect is `main`, which I will argue you
should have blocked to require a passing `ci`, and potentially reviewers to
merge in.  Therefore you can't even push to `main` anyways.

To just push to the branch you are currently on each and every time and never
see this error again, you can run this to configure git to always push to your
current branch.

``` bash
git config --global push.default current
```