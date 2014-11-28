---
title: Text rendering in Sublime Text
layout: post
tags: [programming, sublime text]
comments: true
share: true
---
I love Sublime Text. Unless I really need to use IDE-exclusive features, ST is my go-to choice to jotting down letters and symbols. Although text rendering on Windows looked fine for me, I discovered a way to make it even better.

Go to &#8220;Preferences -> Settings &#8211; User&#8221; and add this, to turn on DirectWrite:

{% highlight json %}
{
    "font_options":  
    [  
        "directwrite"  
    ]
}
{% endhighlight %}

Put an appropriate comma, if required, to make it valid JSON. Also remember to update your GPU drivers because your ST now renders hardware-accelerated text.