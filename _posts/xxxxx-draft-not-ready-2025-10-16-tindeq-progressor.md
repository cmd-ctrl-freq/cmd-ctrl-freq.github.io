---
title: "Web: Free Tindeq Progressor?"
author: David (Mitch) Fentz
date: 2025-10-16 20:00:00 +0800
categories: [Web]
tags: [Web]
---

If you want to skip to infosec content, click here for the [TLDR](#vuln-tldr).

![Tindeq Vuln](/images/tindeq/tindeq_product.png)
### What is the Tindeq Progressor?

The Tindeq Progressor 500 is perhaps the most useful device on the market at the time of this blog post when it comes to collecting data for progressively overloading overcomming isometrics. It was intended to be used for climbers training their grip, but given that it's just an inline force meter, it can be used in MANY isometric movements with a little creativity. 

It's got an assocaited smartphone application which allows for users to watch their force output without looking at the device itself, and the bluetooth protocol that it uses is open.

So I got one, and while looking over the company's website in an attempt to find documentation on the device, I also found the following...

## Vuln TLDR; 

The Tindeq.com site had a sitemap.xml file that lead to product pages for replacement products. Any user could add these products to their cart for $0, and presumably place an order for them. I stopped short of actually placing an order. 

![Tindeq Vuln](/images/tindeq/tindeq_vuln.gif)

This isn't a wordpress issue, or an issue with the payment processing they are using, or a vuln in any of the underlying technology they are using, so I would classify this as a Business Logic flaw. It's pretty technically boring, but it's rare that I run across stuff like this in the wild so I figured I would document it. 