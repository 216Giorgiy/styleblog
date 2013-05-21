---
layout: post
title:  "New color settings for XAML and User Types"
date:   2010-05-04 18:42:00
---
Yesterday I added support for XAML and a couple more "user types" settings. Below are some examples using Damien Guard's [Twilight](http://studiostyles.info/schemes/twilight) theme (based on the TextMate theme of the same name).

### XAML
![XAML example](/images/2010/05/xaml.png)

I've automatically updated existing themes to use XML colors for XAML. As you can see from the bright red and blue highlighting above, authors will probably need to tweak some colors manually.
If you're creating a new color scheme, you'll see a button to "Copy colors from XML" when you're editing XAML colors. This should save you a bit of time if you want your XAML to look mostly like your XML.

![copy XAML example](/images/2010/05/copy.png)

### More "User Types"

I've also added support for delegates and value types, shown below.

![User Types](/images/2010/05/user-types.png)

For existing themes, these new settings have been automatically set to the same color as the "User Types" setting.