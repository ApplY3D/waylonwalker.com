---
content: ''
cover: ''
date: 2022-02-09
datetime: 2022-02-09 00:00:00+00:00
description: 'Samba is an implementation of the smb protocol that allows me to setup
  network Samba is an implementation of the smb protocol that allows me to setup network
  I '
long_description: 'Samba is an implementation of the smb protocol that allows me to
  setup network Samba is an implementation of the smb protocol that allows me to setup
  network I think the homelab is starting to intrigue me enought to dive into the
  path of I think the '
now: 2022-05-07 21:32:25.892084
path: pages/til/simple-samba.md
slug: til/simple-samba
status: published
super_description: Samba is an implementation of the smb protocol that allows me to
  setup network Samba is an implementation of the smb protocol that allows me to setup
  network I think the homelab is starting to intrigue me enought to dive into the
  path of I think the homelab is starting to intrigue me enought to dive into the
  path of To get goind I am going to make a directory  To get goind I am going to
  make a directory  Install samba, open the firewall, and edit the  Install samba,
  open the firewall, and edit t
tags:
- linux
- linux
- linux
templateKey: til
title: Simple Samba Share Setup
today: 2022-05-07
year: 2022
---

Samba is an implementation of the smb protocol that allows me to setup network
shares on my linux machine that I can open on a variety of devices.

I think the homelab is starting to intrigue me enought to dive into the path of
experimenting with different things that I might want setup in my own home.
One key piece of this is network storage.  As I looked into nas, I realized
that it takes a dedicated machine, or one virtualized at a lower level than I
have capability for right now.


## Humble Beginnings

To get goind I am going to make a directory `/srv/samba/public` open to anyone
on my network.  I am not going to worry too much about it, I just want
something up and running so that I can learn.

Install samba, open the firewall, and edit the `smb.conf`
```
sudo apt install samba samba-common-bin
sudo ufw allow samba
sudo nvim /etc/samba/smb.conf
```

I added this to the end of my `smb.conf`

```
[public]

comment = public share, no need to enter username and password
path = /srv/samba/public/
browseable = yes
writable = yes
guest ok = yes
```

Then I made the `/srv/samba/public` directory and made it writable by anyone.

```
sudo mkdir -p /srv/samba/public
sudo setfacl -R -m "u:nobody:rwx" /srv/samba/public/
```

## Windows, yes windows

I have a windows desktop in my office, primarily for my wife to run premiere
pro, and my son to play Minecraft.  I walked over to it, opened the file
explorer, and ernt to `\\<my-local-ip>`.  It asked for the username and
password, I typed in the username and password of the linux device I have the
share running on, and I was in.  Right there I could see the Public folder.  I
opened it and made a files successfully.