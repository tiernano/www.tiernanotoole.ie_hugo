+++
aliases = []
date = "2018-07-04T17:10:16+00:00"
publishdate = "2018-07-04T17:00:00+00:00"
published = true
slug = "moving-the-site-to-hugo"
tags = ["blogging"]
title = "Moving the site to Hugo"

+++
After a LOT of messing with [Jekyll](https://jekyllrb.com/), i have finally moved to [Hugo](https://gohugo.io/)! There are a few things that don't fully work yet, and there will be updates to the site soon enough, but for the moment, I am happy... Its also a LOT faster to build than Jekyll, and less dependencies... Happy days!

[update] I though i should probably update this post with a bit more information around hows its built, why i moved to Hugo, and some more links, etc. 

First, it is currently being built using [Forestry.io](http://www.forestry.io). I use it for both editing the documents (mind you i also use VScode for this too) and ii also builds the site now too. I have 2 Github repos. [The main code](https://github.com/tiernano/www.tiernanotoole.ie_hugo) and the [Static HTML](https://github.com/tiernano/www.tiernanotoole.ie_hugo_static). When i check into Github, it it sends a webhook to Forestry, which then pulls the latest code and builds the site, and then checks the resulting files into the static HTML repo. Currently its a manual process to get it on to my server. This site is currently hosted on a server in London with my own [AS204994](https://www.tiernanotoole.ie/2018/04/01/as204994-own-ip-space-and-anycast.html) serving the pages. I plan on adding other servers to the list so its proper any-cast, but currently only 1 is running as a web server currently (there are 4 others, if you include the one in the house: 3 in total hosted on [Vultr](https://www.vultr.com/?ref=6925432) (LON, FRA, NYC) 1 in [DevCapsule](http://www.devcapsule.com) and then the house) but that is my next challenge...

Next question is why? Well, over the last few months, its taking longer and longer to build the site using Jekyll... Its also getting more painful to maintain, since you have to mess with dependancy hell when updates come out... 

{{< cloudinary src="v1530736063/jekyll-build-docker.png">}}

then when it finally builds, it takes more than 4 min in most cases...

{{< cloudinary src="v1530736221/jekyll-build-docker-time.png">}}

Now, in all fairness, this is building on a clean machine with no bundle caching, and i did have bundle caching at some stage, but its still takes a long enough (30-40 seconds in some cases) to build compared to Hugo:

{{< cloudinary src="v1530736323/hugo-build.png">}}

the other big advantage is that Hugo arrives in a single EXE (or other binary format for other platforms) and runs on Windows without any extra stuff to install... drop the EXE in your path, cd into the folder, and `hugo serve` and you have a web server running with your files... if you want to deploy them, run `hugo` and it builds the project and sticks it in your `public` folder. Do what you want with it from there! Happy day! 

So, finally, some links i have found useful while building this site. 

* [The Hugo Documentation site](https://gohugo.io/documentation/) should be your first point of call... Lots of handy stuff in there...
* [Adding Search with Algoia](https://forestry.io/blog/search-with-algolia-in-hugo/) Since the site is static, search doesn't currently work... but with the help of a hosted service named [Algoia](https://algolia.com/) you can get around that easily enough...
* [Turn your static site into a JSON API](https://forestry.io/blog/build-a-json-api-with-hugo/): I am thinking of tweaking the Computers pages (they stopped working as planned when i moved over) and using a JSON API for it... Same with the tools list... 
* [Short Codes](https://gohugo.io/content-management/shortcodes/): Hugo doesn't really have a plugin model like Jekyll did... but there is still a lot of interesting things you can do... Short codes lets you write custom HTML that gets generated when you put in a particular block of code... Have a look at the link on the bottom of the page to see the code used to generate this page. 
* [Cloudinary](https://cloudinary.com/invites/lpov9zyyucivvxsnalc5/odc5hvptjxifri3jusn9): Since moving so static sites, i have found images to be a pain in the ass... Found these guys the other day, and they integrate well with Forestry. and their free version works grand for smaller sites... 

so, any comments, questions, etc, just leave a message below. and dont forget to [subscrbe to the RSS](http://feeds.feedburner.com/tiernanotoole) for updates as they come out! 

[UPDATE 2]. So, with the help of [Github Webhooks](https://developer.github.com/webhooks/) and the [webhook project](https://github.com/adnanh/webhook), this site auto deploys to 5 different servers and is currently being served on 4... Dub is not fully live yet... happy days!