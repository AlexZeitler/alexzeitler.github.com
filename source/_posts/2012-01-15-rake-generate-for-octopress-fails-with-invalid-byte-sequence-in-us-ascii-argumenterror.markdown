---
layout: post
title: "rake generate for octopress fails with invalid byte sequence in US-ASCII (ArgumentError) "
date: 2012-01-15 23:53
comments: true
categories: [rake,octopress]
---
If you're receiving an error similar to this
```
[~/Documents/alexzeitler.com]$ rake generate         [source][ruby-1.9.2-p290] 
## Generating Site with Jekyll
unchanged sass/screen.scss
Configuration from /Users/alex/Documents/alexzeitler.com/_config.yml
Building site: source -> public
/Users/alex/.rvm/gems/ruby-1.9.2-p290/gems/jekyll-0.11.0/lib/jekyll/convertible.rb:29:in `read_yaml': invalid byte sequence in US-ASCII (ArgumentError)
	from /Users/alex/.rvm/gems/ruby-1.9.2-p290/gems/jekyll-0.11.0/lib/jekyll/post.rb:39:in `initialize'
	from /Users/alex/Documents/alexzeitler.com/plugins/preview_unpublished.rb:23:in `new'
	from /Users/alex/Documents/alexzeitler.com/plugins/preview_unpublished.rb:23:in `block in read_posts'
	from /Users/alex/Documents/alexzeitler.com/plugins/preview_unpublished.rb:21:in `each'
	from /Users/alex/Documents/alexzeitler.com/plugins/preview_unpublished.rb:21:in `read_posts'
	from /Users/alex/.rvm/gems/ruby-1.9.2-p290/gems/jekyll-0.11.0/lib/jekyll/site.rb:128:in `read_directories'
	from /Users/alex/.rvm/gems/ruby-1.9.2-p290/gems/jekyll-0.11.0/lib/jekyll/site.rb:98:in `read'
	from /Users/alex/.rvm/gems/ruby-1.9.2-p290/gems/jekyll-0.11.0/lib/jekyll/site.rb:38:in `process'
	from /Users/alex/.rvm/gems/ruby-1.9.2-p290/gems/jekyll-0.11.0/bin/jekyll:250:in `<top (required)>'
	from /Users/alex/.rvm/gems/ruby-1.9.2-p290/bin/jekyll:19:in `load'
	from /Users/alex/.rvm/gems/ruby-1.9.2-p290/bin/jekyll:19:in `<main>'
```

when running ```rake generate``` for octopress, add this to your ```.profile``` or ```.zshrc``` etc.

```
LANG=en_US.UTF-8
LC_ALL=en_US.UTF-8
```
 