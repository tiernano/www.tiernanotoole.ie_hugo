+++
aliases = []
date = "2018-09-06T16:00:00+01:00"
publishdate = "2018-09-06T16:00:00+01:00"
published = true
slug = "adding-netgear-lb2120-to-homelab"
tags = ["Networking", "Homelab"]
title = "Adding a Netgear LB2120 to the homelab"

+++
A few months back, Three Ireland came out with an [LTE broadband offer](https://www.three.ie/plans/mobile-broadband/bill-pay/): Unlimited* LTE broadband for EUR30 per month. It did come with a 18 month contract, but I pulled the trigger and got it as a backup link. I picked this up in the local Three store, and they had a couple of options for modems: a couple of Huawei mobile Wifi hotspots ([E5573](http://geni.us/N0XLRN) or [E5577](http://geni.us/xmsJ4I)) or a [Huawei B525](http://geni.us/AC1IUa) Modem, which is designed for home use. Alternatively, there was a Sim only option, but given the modem was free with the contact, i went with the B525.

{{< cloudinary src="v1536249205/IMG_20180906_164829.jpg" >}}

The B525 is not a bad router, don't get me wrong, but its a **Router**... i already have a few of them, including my [Mikrotik RouterBoard CCR1016-12G](http://geni.us/phtv5Sn), an [EdgeRouter POE](http://geni.us/euTjLI), a [Ubiquiti USG 3](http://geni.us/hArou) and some virtual ones too... yea, don't ask... What i wanted was a modem; no WiFi, no routing, and give me a full, non NATted IP to the internet. There was some mention of some of the Huawei modems being able to be put into bridge mode, but i could not find out how to do it... That's where the [Netgear LB2120](http://geni.us/EJli) comes in.

{{< cloudinary src="v1536249205/IMG_20180906_164846.jpg" >}}

The LB2120 (there are a few differnet models, but mine is the Europe edition) has a Micro SIM Slot,a WAN and a LAN port (both GigE), Power in, Power button and 2 inputs for Aerials.

{{< cloudinary src="v1536249205/IMG_20180906_164852.jpg" >}}

The home page is fairly basic, and gives you all you need: how much data you've used, how much you have left, when the data plan resets, etc.

{{< cloudinary src="v1536249205/LB2120-home.png" >}}

There is also an alerts option, so you can get it to send you an SMS when something happens:

{{< cloudinary src="v1536249205/lb2120-alerts.png" >}}

but the realy handy stuff is under Advanced setting/LAN:

{{< cloudinary src="v1536249205/lb2120-settings.png" >}}

You have the option of using it as a router, or using it in a Bridge. neadless to say, i bridged it and got a fully public IP. Currently, mine is hooked up to the second WAN port of the USG, and is currently serving about 30-40% of the traffic on that network (mostly media devices, IOT stuff, etc). Speed wise, its not bad. 

{{< cloudinary src="v1536249205/lb2120-speedtest.png" >}}

Not as good as a hardwired connection, but its only getting 4 bars, and its about 1km to the nearest cell tower. I do want to get some external aerials for it, to see if i can boost the download/upload speed, but we will see. Also, i plan on changing out the Mikrotik for something else... lets see what i end up with!

\*Unlimited is mobile network speak for 750GB per month... which does not sound very unlimited to me... but, anyway...