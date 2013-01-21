---
layout: post
title: "git push prompts for UserName and Password on GitHub"
date: 2012-02-07 22:33
comments: true
categories: [git,github]
---
If ```git push origin master``` prompts for you UserName when ```<origin>``` is on GitHub, you may need to fix your ```origin``` url, e.g.

```
git remote set-url origin git://github.com/AlexZeitler/node-hands-on.git
```

The correct url is the GitHub url with read/write access (you get it if you click the SSH button):
![image](https://github.com/AlexZeitler/alexzeitler.github.com/raw/source/images/readwriteurl.png)