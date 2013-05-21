---
layout: post
title:  "New &quot;advanced&quot; highlighting"
date:   2010-05-14 20:14:00
---
If things have been a bit quiet for the last 2 weeks, that's because I've been working on the biggest update since the site launched: adding support for more color elements. Check this out:

[![Phosphorescent theme by Jason Kozak](/images/2010/05/advanced.png)](http://studiostyles.info/schemes/phosphorescent)

This is all available now on the website - look for [schemes with the advanced tag](http://studiostyles.info/schemes/supporting/advanced) to see examples that support this feature. Authors can edit their existing schemes to add support for these.

For those of you keeping track, the new color elements include:
* Collapsible and collapsed regions
* Highlighted references
* Inactive selection
* Code outlining
* Errors and warnings
* Excluded code

Many of these elements have one or two things that make them difficult to implement in a web-based editor, which is why they didn't make it into the website before it launched. If I've done a good job implementing them then you won't notice how tricky these were, but for anyone interested here's some more background info.

### "Squiggle" underlines for errors and warnings
This was my first experiment with the [HTML5 canvas](http://diveintohtml5.org/canvas.html), and it was fun. It brought back memories of learning Logo in primary school, where you tell the turtle PEN DOWN, FORWARD 10, RIGHT 3 etc. Who would have thought that would ever come in handy?

I had a go with SVG at first, but after a few failed attempts at a [hack](http://old.nabble.com/Wavy-line-symbol-in-SVG-td15294150.html), I decided to be a real man and draw bitmaps directly to your browser.

![squiggle example](/images/2010/05/squiggle.png)

The squiggles work in Chrome, Safari, Opera and Firefox. If you're using Internet Explorer you'll see a fairly unexciting dashed underline, but you can still edit the colors.

### Code outlining
This was the quite hard to do in HTML & Javascript. I could have gone with SVG or canvas again, but there wouldn't have been a fallback for IE which accounts for 1/3 of the traffic on Studio Styles. So it's all basically &lt;div&gt;s with borders. Supporting various fonts and font-sizes was tricky too - I wanted it to work with other fonts eventually, and of course if you browse with a larger font size everything should still line up.

### Alpha compositing
Visual Studio uses opacity for some of the elements, e.g. Selected Text, Collapsible Region (the foreground color is used in the margin background when you hover over a region). Previously I had kludged these using a transparent &lt;div&gt; overlay and let the browser do the work, but it was messy. I switched to manually calculating the combined background colors using the A over B algorithm here. It's much more satisfying.
