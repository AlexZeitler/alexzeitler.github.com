---
layout: post
title: "Permission denied (publickey) when trying to access repository on GitHub"
date: 2012-01-13 18:10
comments: true
categories: [git, ssh] 
---
If you already own a GitHub account and try to clone from or push to a repository on GitHub you may receive a 

```
Permission denied (publickey)
```

error.

This may be the case if you have set up a new machine without having installed your existing ssh key properly.

To do so, just copy your private key to your ~/.ssh directory and call:

```
$ ssh-add ~/.ssh/id_rsa
``` 

whereas id_rsa is the name of your ssh key.

Another reason why you fail, may be a missing .config file in your ~/.ssh folder.

If this is the case, just create it and paste the following into it:

```
Host github.com
  User git
  Port 22
  Hostname github.com
  IdentityFile ~/.ssh/id_rsa
  TCPKeepAlive yes
  IdentitiesOnly yes
```