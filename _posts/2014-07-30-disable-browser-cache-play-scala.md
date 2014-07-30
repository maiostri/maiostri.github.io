---
layout: post
title: Disable browser cache in play framework
tags: [Play, Scala, HTTP]
---

Prevent the browser to cache every page could be very useful in dev enviroments. Here is a quick tip on how disable it on Scala with Play! using the
HTTP header **Pragma** (or the new **Cache-Control** header).
More details about these HTTP Headers can be found [here](//http://www.w3.org/Protocols/rfc2616/rfc2616-sec14.html).

In your Global object, add the followings methods

{% gist maiostri/90ed595b368a46ce3ff8 %}

The **NoCache** function is reponsible for adding the header in the request, and the **onRouteRequest** is the
responsible method for intercepting every request routed by Play.

Hope it could be useful for you!
