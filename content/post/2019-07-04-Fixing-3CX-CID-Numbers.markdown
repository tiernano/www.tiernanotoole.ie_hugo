+++
aliases = []
date = "2019-07-04T17:00:00+01:00"
publishdate = "2019-07-04T17:00:00+01:00"
published = true
slug = "fixing-3cx-cid-numbers"
tags = ["VoIP", "Homelab"]
title = "Fixing CID (Caller ID) on incoming calls with 3CX"

+++

In a [previous post](https://www.tiernanotoole.ie/2018/07/24/finally-going-all-in-on-voip.html) i talked about going all in on VoIP in the house. Its been nearly a year now, and other than some minor issues related to the VoIP Server being turned off accidently, or a screw up on my end, all is going well. But, one thing i did notice was related to incoming calls and caller Id, specifically on my [SIP2SIM](https://www.aa.net.uk/voice-and-mobile/sip2sim/) card. Essentially, the country code was wrong: for example: Incoming calls from the [Virgin Media](https://www.virginmedia.ie) trunk just show as local numbers (for Dublin, for example, it would so 01xxxxxxx). Using the [CID reformatting](https://www.3cx.com/docs/cid-reformatting/) feature in 3CX, i managed to change this.

{{< cloudinary src="v1562248733/cid-reformatting.png">}}

All calls that come in starting with 0 are "fixed" and changed to +353 without the 0. When the call comes in though the Sip2Sim card, it does no longer show as a call from the UK, but now shows as a call in Ireland, so all the contact details show correctly! Happy days!