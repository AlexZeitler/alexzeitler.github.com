---
layout: post
title: "Convert SVG to PNG on OS X"
date: 2013-01-21 23:33
comments: true
categories: OSX
---
If you need to convert .svg files to .png, there's a handy command line tool that comes with OS X: qlmanage.

To convert my.svg file to my.png having a width of 1000px just run
{% codeblock %}
qlmanage -t -s 1000 -o . my.svg 
{% endcodeblock %}
