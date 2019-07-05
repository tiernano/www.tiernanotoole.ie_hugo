---
date: 2015-09-30 20:00:00 +0000
tags:
- Networking
- Sophos_UTM
- Hardware
- HomeLab
- Ubiquiti
title: Edge Router, Sophos UTM, DMZ and LAN Networks
slug: EdgeRouter-SophosUTM-DMZ-LAN-Firwwalls
aliases:
- /2015/09/30/EdgeRouter-SophosUTM-DMZ-LAN-Firwwalls.html
- /2015/09/30/edgerouter-sophosutm-dmz-lan-firwwalls.html
disqus_identifier: https://www.tiernanotoole.ie/2015/09/30/EdgeRouter-SophosUTM-DMZ-LAN-Firwwalls.html
disqus_url: https://www.tiernanotoole.ie/2015/09/30/EdgeRouter-SophosUTM-DMZ-LAN-Firwwalls.html

---
 I have been using an [EdgeRouer POE](https://www.ubnt.com/edgemax/edgerouter-poe/) as my main router for most of the network (some of the network still uses [PFSense](http://www.pfsense.org) as a router, but thats being removed soon) for the last few weeks, and i am quite happy with it. I also have a second router, a [Sophos UTM](https://www.sophos.com/en-us/products/unified-threat-management.aspx) VM between my first LAN (essentially a DMZ) and my client LAN (there will be more "LANs" over there soon). The Client LAN is NATed between the DMZ and the LAN, which means anything on the LAN i want to access from the DMZ has to be port forwarded... Ideally, not much from the LAN should be accessible though the DMZ, but in my initial setup, stuff like [Plex](http://www.plex.tv), etc, is...

What i wanted to do was setup a proper firewall between both networks, without the use of NAT... Do do this, i first had to disable th masquerading rules in Sophos:

{{<cloudinary src="v1530620916/20150930-masquerading-off.png">}}

next, on the EdgeRouter, i added a static route to point at the new network:

{{<cloudinary src="v1530620916/20150930-static-route.png">}}

And finally, under firewall rules, i allowed what i wanted to allow (in this case, SSH from any DMZ client (not advised) to my Mac Mini).

{{<cloudinary src="v1530620916/20150930-firewall-rules.png">}}

And that, as they say, is that! So far, so good!