---
canonical_url: https://waylonwalker.com/til/nix-install-java8/
cover_image: https://images.waylonwalker.com/til/nix-install-java8.png
description: With the latest version of minecraft it requires a very new, possibly
  With the latest version of minecraft it requires a very new, possibly I was getting
  this e
published: true
tags:
- cli
- cli
- cli
title: nix rescues modded minecraft night
---

With the latest version of minecraft it requires a very new, possibly the latest, version of java.  Lately we have been getting into modded minecraft and I maintain the server for us.  It's been tricky to say the least.  One hurdle I recently hit involves having the wrong version of java.

I was getting this error trying to get a 1.12.2 forge server running.

> Caused by: java.lang.ClassCastException: class jdk.internal.loader.ClassLoaders$AppClassLoader cannot be cast to class java.net.URLClassLoader (jdk.internal.loader.ClassLoaders$AppClassLoader and java.net.URLClassLoader are in module java.base of loader 'bootstrap')

In researching our errors, I found this on a forum.

> Pre-1.13 Forge only works with Java 8.

I don't write java, or really know how to manage different versions of java, but I have nixpkgs installed and it has a ton of odd stuff like this readily available, so [searching nixpkgs](https://search.nixos.org/packages?channel=21.05&show=jdk8&from=0&size=50&sort=relevance&type=packages&query=java+8) landed me with this.

``` bash
nix-env -iA nixpkgs.jdk8
```

once I had this installed I then just changed out java for the full path to my new nixpkgs.jdk8 java and it worked.

``` bash
/home/walkers/.nix-profile/bin/java -server -Xms${MIN_RAM} -Xmx${MAX_RAM} ${JAVA_PARAMETERS} -jar ${SERVER_JAR} nogui
```

I don't write java or do anything other than host minecraft servers wtih it.  There is probably a better way of maintaining java versions than this, but this worked for me.