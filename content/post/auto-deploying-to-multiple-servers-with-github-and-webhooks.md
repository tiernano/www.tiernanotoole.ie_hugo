+++
aliases = []
date = "2018-07-05T16:40:23+00:00"
draft = true
publishdate = "2018-07-05T20:00:00+00:00"
published = true
slug = ""
tags = ["Tutorial", "Blogging"]
title = "Auto deploying to multiple servers with GitHub and Webhooks"

+++
In yesterdays post, i mentioned that i wanted to try get an auto deploy working for this site. It already builds automagically using Forestry and puts the static HTML into a Github repo, but i needed to manually update the servers hosting the site... Well, not any more!

{{< cloudinary src="/v1530809017/github-webhook.png">}}

using the magic of [Github's Web hooks](https://developer.github.com/webhooks/), the [Webhook project](https://github.com/adnanh/webhook) and a small piece of bash shell script, i have managed to get this auto deploying...

First, Download the Webhook project (its a [Go](https://golang.org/) application, so it works pretty much anywhere). Copy it somewhere on your machine. Next, you need a config. I used the [Github sample config](https://github.com/adnanh/webhook/blob/master/docs/Hook-Examples.md) from the project site and made tweaks to what script to run and what i was passing in.

{{< gist tiernano 1a2329461702b20e347f907b00752abb >}}

next, the script to pull from Github was simple enough:

{{< gist tiernano 005f0211787de9ec73a683d84a7d81ce >}}

Then, its just a matter of running the file:

`./webhook --hooks github.json --verbose`

The `--verbose` tag gives you lots of info, so its handy for testing. and then your app is running and listening on the default port, 9000.

next, head over to your project on Github and go to settings:

{{< cloudinary src="/v1530810063/github-settings.png">}}

select webhooks and add new web hook

{{< cloudinary src="/v1530810063/github-webhook-list.png">}}

Fill in the required details on the page, and click save.

{{< cloudinary src="/v1530810063/github-create-webhook.png">}}

Github will go out and have a chat with the webhook and verify it can send and recieve stuff from the hook. You can see this in the deliveries section:

{{< cloudinary src="/v1530810063/github-webhook-deliveries.png">}}

Clicking on these will show you the headers that were sent, along with the payload, and you can also see the response from your server. Finally, you have the option of resending the payload, just in case anything goes wrong.

So, there you have it. A complete automated deploy across multiple servers! Any questions, leave a comment below! 