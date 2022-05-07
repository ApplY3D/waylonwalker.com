---
content: ''
cover: ''
date: 2022-01-10
datetime: 2022-01-10 00:00:00+00:00
description: I recently paired up with another dev running windows with Ubuntu running
  in I recently paired up with another dev running windows with Ubuntu running in
  Open u
long_description: I recently paired up with another dev running windows with Ubuntu
  running in I recently paired up with another dev running windows with Ubuntu running
  in Open up a terminal and get your required system dependencies using the apt Open
  up a terminal an
now: 2022-05-07 21:32:25.891470
path: pages/til/installing-pipx-on-ubuntu.md
slug: til/installing-pipx-on-ubuntu
status: published
super_description: I recently paired up with another dev running windows with Ubuntu
  running in I recently paired up with another dev running windows with Ubuntu running
  in Open up a terminal and get your required system dependencies using the apt Open
  up a terminal and get your required system dependencies using the apt I like running
  things like this through an ansible-playbook as it give me some I like running things
  like this through an ansible-playbook as it give me some Here is a clip of me getting
  pipx runn
tags:
- python
- linux
- cli
templateKey: til
title: Installing Pipx on Ubuntu
today: 2022-05-07
year: 2022
---

I recently paired up with another dev running windows with Ubuntu running in
wsl, and we had a bit of a stuggle to get our project off the ground because
they were missing com system dependencies to get going.

## Straight in the terminal

Open up a terminal and get your required system dependencies using the apt
package manager and the standard ubuntu repos.

``` bash
sudo apt update
sudo apt upgrade
sudo apt install \
      python3-dev \
      python3-pip \
      python3-venv \
      python3-virtualenv
pip install pipx
```

## Using an Ansible-Playbook

I like running things like this through an ansible-playbook as it give me some
extra control and repeatability next time I have a new machine to setup.

``` yaml
- hosts: localhost
  gather_facts: true
  become: true
  become_user: "{{ lookup('env', 'USER') }}"

  pre_tasks:
    - name: update repositories
      apt: update_cache=yes
      become_user: root
      changed_when: False
  vars:
    user: "{{ ansible_user_id }}"
  tasks:
    - name: Install System Packages 1 (terminal)
      become_user: root
      apt:
        name:
          - build-essential
          - python3-dev
          - python3-pip
          - python3-venv
          - python3-virtualenv
    - name: check is pipx installed
      shell: command -v pipx
      register: pipx_exists
      ignore_errors: yes

    - name: pipx
      when: pipx_exists is failed
      pip:
        name: pipx
      tags:
        - pipx
```

## video clip

Here is a clip of me getting pipx running on ubuntu 21.10, and running a few of
my favorite pipx commands.

![installation video](https://images.waylonwalker.com/pipx-install-ubuntu.gif)