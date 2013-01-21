---
layout: post
title: "Restarting node.js server automatically when source code changes"
date: 2013-01-21 23:46
comments: true
categories: nodejs
---
During development, you're constantly changing your source files. Normally that would require you to call something like 

```
$ node server.js
```
everytime you change one of your source files.

A simple workaround is to 
```
$ sudo npm install supervisor -g
```
Now you run
```
$ supervisor server.js
```
Only once and everytime your source code changes, your development server gets restarted by supervisor automatically.