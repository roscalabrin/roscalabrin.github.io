---
layout: post
title:  "HTTP: Looking Back and Forward"
date:   2016-08-1 8:20:56 -0600
categories: blog
---

This past May I joined Turing School of Software & Design.  After roughly four weeks of intense classes and projects, I was tasked with building a simple server and get deep in the trenches of understanding of how HTTP works.

Since then, I have found myself spending more and more time getting engrossed in the world of web applications through articles and videos. Although I had a pretty basic idea of the general structure of how the Internet works, learning about the intricacies and nuances of what goes on behind the scenes has continued to fascinate me.

In that context, I stumbled across the oncoming HTTP/2 , the solution to overcome many of the current drawbacks of HTTP/1.1. The evolution of HTTP itself raises questions as far as how are we looking into the future and how HTTP can become more efficient and robust. 

First let’s take a step back before looking into the promises of HTTP/2.
HTTP is the protocol that defines a set of standards for the communication between Web-servers and clients. 

The first documented version of HTTP was released back in 1991, followed by revisions in 1996 and 1997. However, there hasn’t been any major changes since 1997, which means that the most recent version of HTTP has served the web for an eternity

As I was writing this blog post, I was trying to remember what the web was like back in 1997.
Let’s just start by mentioning that Google.com didn’t exist in 1996! The domain was in fact registered in September, 1997. I also browsed through  [WaybackMachine](http://archive.org/web/) just to get a visual representation of what was going on almost 20 years ago. Here’re just two examples: 


<img src="/assets/yahoo.png" width="600" height="400">
<br />
<br />
<img src="/assets/whitehouse.png" width="600" height="400">

Websites and applications have and continue to become far more complex.

Although there’s nothing wrong with HTTP, and the fact that it’s been around for so long proves that it works. This doesn’t mean that there’s not room for improvement.

While developers have created solutions to the shortcoming of HTTP/1.1, for instance, concatenating files, sprinting images, and domain sharing. HTTP/2 preposition is to provide an alternative solution focusing on rethinking key concepts of the protocol. 

The goal of HTTP/2 is for performance. Mainly, tackling the end-user perceived latency and the limitations of a single request per TCP connection. With HTTP/1.1, browsers open multiple TCP connections to handle multiple requests simultaneously. The problems that come with multiple requests are basically TCP congestion and duplication of data transmission.

As of 2016, [HTTP/2 is used by 9% of all websites.](https://w3techs.com/technologies/details/ce-http2/all/all) 
Some of the most popular sites using HTTP/2  are Google.com, Facebook.com, YouTube.com, Yahoo.com, Wikipedia.org, Twitter.com.

<img src="/assets/growth_chart.png" width="600" height="400">

HTTP/2 is not a new protocol. As Mark Nottingham (HTTPbis WG Chair) pointed out “...we are not replacing all of HTTP – the methods, status codes, and most of the headers you use today will be the same. Instead, we’re redefining how it gets used “on the wire”, so it’s more efficient, and so that it is more gentle to the internet itself…”

An important distinction to make is that HTTP/2 is not starting over. It takes what already works on HTTP/1.1 and builds on top of it.
The two things that stuck out to me are the new binary framing layer and the server push.

In a nutshell, with the binary framing layer, client and server can disintegrate HTTP payload into small independent sequences of frames. Multiple streams are mixed and transmitted over a single TCP connection, and reassembled at the other end. Without getting too much in detail, this is an interesting approach to address the multiple requests drawback of HTTP/1.1, and could be a key part of making the protocol more robust to respond to the complexities and traffic increase that have grown exponentially.

The idea that servers can send information the hasn’t yet been requested, but is anticipated in future requests, makes me think of our move towards smart technology. 
In general, we’re seeing machines becoming more proactive, and the lines of responsibilities and communication that we have with machines are becoming blurred.

Although this implementation will take time, I believe that HTTP/2 could be the seed of constructing a more robust way of communication through our dearly World Wide Web. 
