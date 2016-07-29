---
title: Pi Woes 1 - Getting HTTP 403 Forbidden error with urllib.request
layout: post
tags: [programming, python, raspberry pi]
comments: true
share: true
categories: blogpost
summary: 'Sensors is not really my forte'
---
I was trying to send a set of sensor inputs to one of my droplets hosted on Digital Ocean. I had a rolled out a simple node.js/Ghost image which I have been using to serve a few ExpressJS applications alongside. While I was using urllib.request module of the Python to send the data to the express.js application which is behind nginx.

I was able to send the request through my browser but it was failing through the urllib module with HTTP 403 Forbidden error.

After a little Google-fu I found that it maybe because of no headers being sent along with the HTTP request. But I needed to know which of the header was so critical that nginx was even rejecting the request outright.

With a little hit and trial, I found that it was *User-Agent*.
