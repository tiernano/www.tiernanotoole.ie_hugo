---
layout: computers
title: Godbox
sitemap:
  priority: 0.7
  changefreq: weekly
aliases:
  - /Computers/godbox.html
---
# GodBox V1

The GodBox is my main Hyper-V server and backup workstation. Its specs are as follows:

* Dual [Intel Xeon E5520][1] processors at 2.26Gz each. They are Quad core and are Hyper Threaded... Windows sees 16 processors!
* 84Gb RAM ([DDR3 ECC](https://amzn.to/2KDA0ec))
* 2 300GB [Western Digital VelociRaptors][2] in RAID 0 for boot.
* 4 hard drives in a storage pool. 2X1TB [Western Digital Green](https://amzn.to/2MR8mH4) Drives, 2Tb [Seagate Barrcuda Green](https://amzn.to/2u8gpHD) drive, 500GB Samsung [Spinpoint drive](https://amzn.to/2MPB8Yt). These are connected to a Dell Perc H200, but no raid is used on the card.
* Connected to a DVI KVM switch and used on a [28 Inch Dell 4K Monitor][3]
* Runs [Windows Server 2016 Datacenter](https://www.microsoft.com/en-us/cloud-platform/windows-server), Hyper-V and has a few VMs running all the time...
* [CPU-Z information here](https://valid.x86.fr/krg7cf)

Some old photos of the machine are seen here:

{{<cloudinary src="v1530799664/krg7cf.png">}}

{{<cloudinary src="v1530620911/godboxv1-cpuinfo.png">}}
    
{{<cloudinary src="v1530620868/tumblr_n15uoaNSnY1s6snd0o1_1280.jpg">}}



[1]: http://ark.intel.com/products/40200/Intel-Xeon-Processor-E5520-8M-Cache-2_26-GHz-5_86-GTs-Intel-QPI
[2]: https://amzn.to/2u9KFC0
[3]: https://amzn.to/2ze6GoZ