---
date: 2015-08-10T11:40:00Z
tags:
- Hardware
- Storage
title: ZFS Home storage pool
slug: ZFS-Home-dir
disqus_url: https://tiernanotoole.ie/2015/08/10/ZFS-Home-dir.html
disqus_identifier: https://tiernanotoole.ie/2015/08/10/ZFS-Home-dir.html
aliases:
- 2015/08/10/ZFS-Home-dir.html
- 2015/08/10/zfs-home-dir.html

---
 
 
 
 
 
 
 

Over the weekend, my [BTRFS][1] pool for my /home directory on Linux failed... Not sure what happened, but it made me
do something i wanted to do for a while: Build a [ZFS][2] pool for my home dir.

First things first, the pool consists of 4 2Tb hard drives and 1 128Gb SSD. Its setup in RAIDZ1 (equivilent of RAID 5)
and then the SSD is set for caching.

To create the pool i ran

	zpool create home raidz sda sde sdf sdg

then, to add the cache drive

	zpool add home cache sdd

the pool (in my case) got mounted to /home, and then i restored my backup to it. to do some tests, i can the
following...

{{< gist tiernano 638891a7d9acac8e396f >}}



614MB/s write and 5.3GB a second read is nothing to be sniffed at! :)


[1]:https://btrfs.wiki.kernel.org/index.php/Main_Page
[2]:https://en.wikipedia.org/wiki/ZFS
