---
date: 2015-05-20 08:12:00 +0000
tags:
- Networking
- VMWare
title: Quick tip for internet facing ESXi servers
slug: quick-tip-for-internet-facing-esxi
aliases:
- 2015/05/20/quick-tip-for-internet-facing-esxi.html
disqus_identifier: https://www.tiernanotoole.ie/2015/05/20/quick-tip-for-internet-facing-esxi.html
disqus_url: https://www.tiernanotoole.ie/2015/05/20/quick-tip-for-internet-facing-esxi.html

---
 Quick tip for all you with internet facing [VMWare ESXi][1] Hosts. I
have just got my hands on a box on the [Hetzner][2] network (more on
that later) and using their LARA system i installed ESXi on it. All was good, then I tried login in a couple hours later and i kept getting errors about my password being wrong... So, i tried a few more times,  got pissed off and rebooted the box (had to do a hard reboot, since i couldn't even get in over KVM). I though this was a hardware issue, or a config issue, and left it... yesterday, i had the console open most of the day, and when looking at something i noticed this:


{{<cloudinary src="v1530620877/20150520-esxi-login-errors.png">}}

Well, that's why I couldn't login! So, tip: create a second user account, name it something other than root, give it a secure password and use that to login to your ESXi box. Ideally, your ESXi box should be behind a firewall, but in the case of a dedicated server, that may not be financially feasible... Hope this helps someone!

[1]:http://www.vmware.com/products/vsphere-hypervisor
[2]:http://www.hetzner.de/en