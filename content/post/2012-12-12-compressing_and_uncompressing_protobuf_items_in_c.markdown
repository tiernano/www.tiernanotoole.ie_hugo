---
date: 2012-12-12T11:29:32Z
redirect_from:
- /2012/12/12/compressing_and_uncompressing_protobuf_items_in_c#.html
tags:
- Programming
- Code
- HowTo
title: Compressing and UnCompressing Protobuf items in C#
slug: compressing_and_uncompressing_protobuf_items_in_c
aliases:
- 2012/12/12/compressing_and_uncompressing_protobuf_items_in_c.html
- 2012/12/12/compressing_and_uncompressing_protobuf_items_in_c.html
disqus_identifier: https://www.tiernanotoole.ie/2012/12/12/compressing_and_uncompressing_protobuf_items_in_c.html
disqus_url: https://www.tiernanotoole.ie/2012/12/12/compressing_and_uncompressing_protobuf_items_in_c.html

---
 Part of a project i am working on required sending large amounts of data between different instances. To get this to work efficially, we started using the [ProtoBuf][1] using [ProtoBuf-net][2] in .NET. but the files where still quite large (17mb, give or take). So, we looked into compression...

here is some examples of how we managed to compress the protobuf files. We got some decient compression: 3mb files, down from 17mb. very happy.

to compress an object (obj) and write to a temp file (tmpfile):


{{< gist tiernano 4267147 >}}


to decompress the object back to a known type:

{{< gist tiernano 4267157 >}}


[1]:http://code.google.com/p/protobuf/
[2]:http://code.google.com/p/protobuf-net/