---
canonical_url: https://waylonwalker.com/til/linux-swap/
cover_image: https://images.waylonwalker.com/til/linux-swap.png
description: 'If you ever end up on a linux machine that just does not have enough
  ram to If you ever end up on a linux machine that just does not have enough ram
  to You can '
published: true
tags:
- linux
title: Create a Swapfile on Your Linux Machine
---

If you ever end up on a linux machine that just does not have enough ram to suffice what you are doing and you just need to get the job done you can give it some more swap.  You can look up reccomendations for how much swap you should have this is more about just trying to get your job done when you are almost there, but running out of memory on the hardware you have.

## make the /swap file

You can put this where you wish, for this example I am going to pop it into
`/swap`

```bash
sudo fallocate -l 4G /swap sudo chmod 600 /swap sudo mkswap /swap sudo swapon /swap
```

## make sure that your swap is on

You can make sure that your swap is working by using the `free` command, I like using the `-h` flag to get human readable numbers.

```bash
❯ free -h
               total        used        free      shared  buff/cache   available
Mem:            15Gi       5.5Gi       4.9Gi       458Mi       5.2Gi       9.3Gi Swap:          4.0Gi          0B       4.0Gi
```


  <div class="onelinelink-wrapper">
      <a class="onelinelink" href="https://waylonwalker.com/reset-ipython/">
          <img style="float: right;" align='right' src="https://images.waylonwalker.com/reset-ipython-og_250x140.png" alt="article cover for 
 Reclaim memory usage in Jupyter
"/>
          <p><strong>
 Reclaim memory usage in Jupyter
</strong></p>
      </a>
  </div>


> I also used this trick in this article to give my python process a bit more oompf and get it on home.