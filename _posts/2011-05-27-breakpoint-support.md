---
layout: post
title: "Breakpoint support"
date: 2011-05-27 16:30:00
---
I just added support for changing breakpoint colors—you'll find it in the Advanced highlighting section.

![breakpoints](/images/2011/05/breakpoints.png)

This is the [nSolarized](http://studiostyl.es/schemes/nsolarized) theme by Chris Nicola

I spent a bit of time getting it to change the circle and arrow colors too, but then I realised Visual Studio doesn't actually support that. Whoops.

It looks like VS just uses bitmaps, which is why you get nasty aliasing effects around the circle when you use a darker color for the indicator margin.

It also means if you choose anything other than the default breakpoint maroon and yellow colors, it's likely to look a bit strange. But hey, it's there if you want to use it!