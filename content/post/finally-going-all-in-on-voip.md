+++
aliases = []
date = "2018-07-24T17:25:19+01:00"
publishdate = "2018-07-24T17:30:00+01:00"
published = true
slug = ""
tags = ["VoIP"]
title = "Finally going all in on VoIP"

+++
After many years, I am finally trying to move to a proper VoIP system for the house. This post will explain what I am using, how I am setting it up, and some other details you might (or might not) find useful.

First, backstory. I have been interested in [VoIP][6] for many years. The first post I wrote about Ito this site was [here back in 2012][1], but I had posted about it on [my other site back in 2008][2]. It got my attention years ago as a way of saving money on calls, but in recent times, that has changed a little, mainly because most providers gives you calls for free (my mobile and land lines both come with unlimited calls and with my mobile, I can make them anywhere in Europe). The new reason I am interesting in VoIP is consolidation: I currently have 3 mobile phone numbers, at least 1 landline dedicated to me in the house, plus a work landline. I want to be able to pick up any phone and make a call, and it show as coming from my main number. Or a call comes in and i can pick it up from any of my phones... And that is what i am trying to do here... I (will) have some of it working, but some parts are still missing... 

The parts I have (or will have) working are as follows:

* my land line number in the house is being ported to [Virgin Media's](4) VoIP service. So, thats not stuck in an analog world any more!
* The house phone now has a VoIP adapter allowing the standard analog phone make VoIP Calls

{{< cloudinary src="v1532448981/31n6elDThZL._SL500_AC_SS350_.jpg">}}

* There is a company in the Netherlands called [ZeroPlex][7] who have a VoIP over GSM service. Essentially, the SIM they give is connected to your own SIP trunk. You can set it up to allow all calls to go though your SIP trunk, only incoming or only out going. I found their contact though [Reddit](https://reddit.com) but they may be able to help if you drop them an email.

* All VoIP traffic in the house is routed though [3CX](https://www.3cx.com). 

{{< cloudinary src="v1532448953/3cx-dashboard.png">}}

* I have a couple of SIP trunks hooked up to 3CX: Virgin Media, Zeroplex (they redirect the NL number is sent over this, and i can make calls though this trunk too), [Twilio][3], which i use for transient numbers, and [Sip Discount](https://www.sipdiscount.com) which offers really cheap calls. 
* Phone wise, i use a [Ubiquiti UVP-Executive](https://www.ubnt.com/unifi-voip/overview/) desk phone, the SIM card, and the [3CX client][8] on mobile (Either iPhone or Android). 

{{< cloudinary src="v1532448953/unifi-voip-phone-exec-features-hdtouchscreen.jpg">}}

So, all in, Im about 50% of the way there... As of the time of this post, the SIM is still in the mail and the phone numbers are not ported to Virgin Media... yet... Tomorrow they should be, and over the next few days there will be some tweaking to get it working correctly... I will probably have some updates over the coming week...

[1]:https://www.tiernanotoole.ie/2012/09/11/voip-stuff.html
[2]:https://blog.lotas-smartman.net/voip-in-ireland/
[3]:http://www.twilio.com
[4]:http://www.virginmedia.ie
[5]:http://www.3cx.ie
[6]:https://www.tiernanotoole.ie/tags/voip.html
[7]:https://www.zeroplex.nl/
[8]:https://www.3cx.com/phone-system/3cxphone/