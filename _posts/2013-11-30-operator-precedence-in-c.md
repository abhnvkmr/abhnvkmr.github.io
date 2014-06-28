---
title: Operator precedence in C++
description: Ambiguity in Operator precedence
layout: post
tags: [programming]
comments: true
share: true
---
Operator precedence and associativity in C/C++ is not too much unintuitive but&#8230;  
<!--more-->

{% highlight c linenos %}
#include <stdio.h>
int main()
{
int i=5;
printf("%d%d%d%d%d",++i,i++,i,i--,--i);
return 0;
}
{% endhighlight %}