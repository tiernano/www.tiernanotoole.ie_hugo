---
date: 2012-10-11T13:09:20Z
tags:
- RouterOS
- Networking
- Firewall
title: RouterOS Blocking Machine access to all but one IP
slug: routeros_blocking_machine_access
aliases:
- 2012/10/11/routeros_blocking_machine_access.html
- 2012/10/11/routeros_blocking_machine_access.html

---
 
 

So, i have a machine on my network, which should be only connecting to the internet though a VPN. I needed to tell my RouterOS box to block all access, except to this said IP address... The following *should* do the trick... YMMV


{% gist 3871919 %}


this will drop any packets from the srcaddress (IP address) that are not for destination dstaddress (IP address). in my case, dstaddress is the VPN server i want to connect to. So, in theory, all packets should just go though the VPN and not leak out in to the rest of the network... again, still testing this so be careful!
