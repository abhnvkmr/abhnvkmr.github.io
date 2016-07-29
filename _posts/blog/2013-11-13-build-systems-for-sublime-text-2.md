---
title: Build systems for Sublime Text 2
layout: post
tags: [programming, sublime text]
comments: true
share: true
categories: blogpost
---
I have been using Sublime Text 2 as my primary text editor. It&#8217;s not as much bloated as Visual Studio or Eclipse and it&#8217;s not as much hard to learn as Vim/Emacs (Sorry folks! I don&#8217;t have that much time to spare). But it&#8217;s highly extensible, customizable and light-weight to use, so this is the program I&#8217;ve been firing since 2012. I&#8217;ve been using Code::Blocks for C++ dev and NetBeans for Java so I needed to rewrite the ST2 build systems for C/C++ and Java. It enabled me to use both the editors without altering my workflow and duplicate installation of compilers.

### C++

  (using Code::Blocks&#8217; mingw32)
{% highlight json %}
{
     "cmd": ["g++", "${file}", "-o", "${file_path}/${file_base_name}"],
     "file_regex": "^(..[^:]*):([0-9]+):?([0-9]+)?:? (.*)$",
     "working_dir": "${file_path}",
     "selector": "source.c, source.c++",
     "shell": "true",
     "variants":
     [
     {
          "name": "Run",
          "cmd": ["start", "C:\\Progra~2\\CodeBlocks\\cb_console_runner.exe", "$file_base_name"]
     }
     ]
}
{% endhighlight %}

###Java
{% highlight json %}
{
     "cmd": ["C:\\Progra~2\\Java\\jdk1.7.0_40\\bin\\javac", "$file"],
     "file_regex": "^(...*?):([0-9]*):?([0-9]*)",
     "selector": "source.java",
     "variants":
     [
     {
          "name": "Run",
          "cmd": ["C:\\Progra~2\\Java\\jdk1.7.0_40\\bin\\java.exe", "$file_base_name"]
     }
     ]
}
{% endhighlight %}  