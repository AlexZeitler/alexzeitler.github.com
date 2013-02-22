---
layout: post
title: "Ctrl+Tab to switch between Windows in OS X Application"
date: 2013-02-22 20:44
comments: true
categories: OSX, KEYBOARD
---

If your OS background is Windows, you're used to use CTRL+TAB to switch between the Windows inside an application. In OS X this doesn't work and some people even suggest to buy third party tools. But there's a simple solution inside the OS X Keyboard settings:

* Open Keyboard settings
* Select "Keyboard & Text Input"
* Find "Move focus to next window"
* Double click the current keyboard shortcut
* Change it by hitting CTRL+TAB on your keyboard

![image](/images/ctrltabonosx.png)

Btw: CTRL+TAB doesn't work in Sublime. You have to edit your .sublime-keymap (SHIFT+CMD+P -> "Key Bindings - User") and paste this:

{% codeblock %}
[
   { "keys": ["ctrl+tab"], "command": "next_view" },
   { "keys": ["ctrl+shift+tab"], "command": "prev_view" }
]
{% endcodeblock %}

