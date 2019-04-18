+++
aliases = []
date = "2019-04-18T18:00:00+00:00"
publishdate = "2019-04-18T18:00:00+00:00"
published = true
slug = "network-update-info-april-2019"
tags = ["Networking", "HomeLab", "Hardware"]
title = "Network Update Info April 2019"

+++
So, this post has been a long time coming! A load of different things to talk about, so lets get started!
 
## GodBox V3

So, for a long time, I have been thinking about GodBoxV3, the replacement to GodBoxV2. And when planning this, i had some ideas of what it should be: 

* Minimum of 2x16 cores (double godboxv2)
* About the same RAM, if not more
* FAST STORAGE!
* Is able to run my twin 30" 4K monitors
* Would like 10Gb/s NICs

Well, It finally happened! I got the machine, built it and, well, its impressive! How did i do with specs? Well...

* 2X [Intel Xeon Gold 6138](https://geni.us/UAgqzO) Processors (20 cores) cooled by 2 [Noctua NH-U12 DX3647](https://geni.us/XRCZ) coolers
* [Supermicro X11DPH-T motherboard](https://geni.us/0B59Jcz) with 2x10Gb links onboard
* 128GB Crucial ECC DDR4 RAM (4 [32GB Sticks](https://geni.us/SM5A))
* 2x 512GB [Samsung 970 Pro NVMe](https://geni.us/VyMiX) drives
* 2x8TB HDDs for extra storage (shucked from 5 [WD My Book 8TBs](https://geni.us/joHV))
* [NVidia GTX1060](https://geni.us/VPGC) graphics
* All in the very nice (and MASSIVE!) [Cooler Master Cosmos II 25th Anniversary edition](https://geni.us/mVKANIN) case.

All is good! Photos, more details and benchmarks coming soon... stay tuned!

## Finally 10Gb/s Networking!

Since GodBoxV3 had a few 10Gb nics, i needed to upgrade the network to support it. I ended up with a [Ubiquiti Networks EdgeSwitch-XG](https://geni.us/FsVA). 16 ports (12 SFP+ and 4 RJ45). The SubperMicro board has 2xRJ45 ports. Due to lack of RJ45 ports, GodBoxV3 is connected to 1, GodBoxV2 is getting a [10Gb card soon](https://geni.us/I0Xqcn), which will be connected to 1 port, and a new Sun Microsystems server (details below) will be getting the last 2... Of the SFP+ ports, 2 are connected to the [EdgeSwitch Lite](https://geni.us/N9HdFtH), 2 to the Synology (it got a [10Gig NIC](https://geni.us/a98pWy) reciently too!) and 2 to the new NAS (again, more details below!)

## Good bye Mikrotik, Hello EdgeRouter 4

Since i was going all Ubiquiti gear (Wifi is Unifi gear) i got rid of the old Microtik and replaced it with a [Ubiquiti ER4](https://geni.us/h5qvyEi). Happy days! Got some plans for this, more details coming soon...

## Updates to BGP Stuff, including IPv6

I lost one VPS in London, but replaced it with a new one from [HostUS](https://my.hostus.us/aff.php?aff=2152). I still use [Vultr](https://www.vultr.com/?ref=6925432), [Packet](https://geni.us/fEXzBRp) and [VServer.Site](https://geni.us/Z8JgBxn) as providers too. I am also adding more and more IPv6 stuff too... There is a [post on AS204994 explaining a lot of this](https://as204994.net/post/quick-overview/). 

## New NAS and more storage!

New NAS got purchased: [QNAP TS-932X](https://geni.us/1BdBXv). I have 5X8TB spinny disks (shucked from 5 [WD My Book 8TBs](https://geni.us/joHV)) + 4 X [500GB WD Blue SSDs](https://geni.us/QuaR6t0). 

## New Servers and cooling updates

Moved lots of stuff around the room... Servers run cooler, and less noisy! happy days! I also got my hands on a very nice looking [Sun Server X3-2](https://geni.us/Ri5Vs). Its a Dual Xeon E5 (currently got quad cores, going to upgrade it to 8 cores) and i think its got 16GB ram and 4x300GB SAS Disks. It also has 4X10Gb nics! ESXi will probably go on here!

## VMWare in the house

Up till reciently, I ran [Hyper-V](https://en.wikipedia.org/wiki/Hyper-V) all round. Its still on GodBox V2 and V3 (v1 has a HDD issue, so its off...), but the main VM hosts (the C6100's) are being migrated to [VMWare ESXi](https://geni.us/tDBSw8z)... Why? Its a learning excersize... We see how it goes...


So, long update... Any questions, comments, etc... shout!
