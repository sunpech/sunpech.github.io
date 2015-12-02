---
layout: post
title: Moved from Blogger to Jekyll
date: '2015-05-25T09:00:00.000-05:00'
author: Steven Suwatanapongched
tags:
- Software Development
- Technology
modified_time: '2015-05-25T09:00:04.552-05:00'
thumbnail: /public/images/blog/tn_blogger-to-jekyll.jpg
image: /public/images/blog/blogger-to-jekyll.jpg
description: "I moved my blog from Blogger to Jekyll."
header-img: /public/images/headers/software_development.jpg
---

I recently made the move from [Blogger](http://www.blogger.com) to [Jekyll](http://jekyllrb.com), hosted on [Github Pages](https://pages.github.com). It was a pretty pleasant conversion too, as Jekyll has a good amount of documenation and support.

I've had a blog since 1999. I've used just about every known blogging technology/platform out there. I've used perl, php, mysql, ASP, MS Access, ASP.NET, C#, MS SQL, Postgres, Ruby on Rails, Heroku, Apache Web Server, IIS, etc to write my own blogging software. I've also used Wordpress, Posterous, Tumblr, Medium, and Blogger, etc as a blogging platform at some point.

![Blogger to Jekyll](/public/images/blog/blogger-to-jekyll.jpg)

### A Cyle of Technologies

After sixteen years, I think it's interesting how things can be so cyclical. Initially, in the late 1990s early 2000s, I didn't have access to a database on my school's server. We students all had a public_html/ folder that would map to a corresponding URL, [http://cs-people.bu.edu](http://cs-people.bu.edu/) with our username. Back then, I used perl and eventually php to write to text files that would be assembled into webpages for my blog. I recall having to use .htaccess files to <i>secure</i> my logins.

After graduating, I built my own linuxbox and moved to use relational databases to host my posts and user logins-- I did open up my web software to friends and family during an era before mySpace and Facebook, your traditional social networks. I did switch tech stacks several times and the conversion between databases was always a bit tricky.

I also ended up trying third party web software/platforms such as [Wordpress](http://www.wordpress.com) and Blogger, as I felt I didn't want to keep switching technologies so much. And by far Blogger was what I stuck with the longest since it was owned by Google.

And yet here I am again with no database and developing/pushing my own code changes as needed to create a static website. I'm hoping this will be the last move for my blog for quite some time.

### Why I chose Jekyll

For years Blogger hasn't really kept up for years with the modern web, so I finally gave up on it and moved to Jekyll. Here are some of the reasons for why I chose Jekyll.

* I didn't need a user interface to write blog posts. Git and markdown is sufficient.
* I wanted to own my own data.
* I wanted more control on customizing the look and feel of the site.
* I didn't want to pay money for any hosting.

### Conversion Process

First thing you'll need to do is have [ruby](https://www.ruby-lang.org/en/) installed on your machine. Then just install the Jekyll gem.

{% highlight bash %}
	gem install jekyll
{% endhighlight %}

This should all work fine if you are using OS X or some flavor of Linux-- I'm not sure about Windows OS.

If you want to host Jekyll for free on [Github Pages](https://pages.github.com), you'll of course need to have a [Github](https://github.com) account. Your <i>username</i> will be what you use. For example: mine is located at [sunpech.github.io](http://sunpech.github.io), which should redirect you to this domain. But the actual repo can be found at [github.com/sunpech/sunpech.github.io](https://github.com/sunpech/sunpech.github.io)-- please excuse the mess.

There is a way to [export Blogger](http://import.jekyllrb.com/docs/blogger/) into an xml document containing all your posts. See screenshot below.

![Export Blogger](/public/images/blog/screenshot_export-blogger.jpg)

Jekyll has some great documenation on [blog migrations](http://jekyllrb.com/docs/migrations/). Specifically, just use [this one](http://import.jekyllrb.com/docs/blogger/) to import from Blogger.

From there, just drop the converted markdown files into _posts/ in your jekyll project directory and you have a basic static site ready to go!

#### More Info

* [Setting up a custom domain with GitHub Pages](https://help.github.com/articles/setting-up-a-custom-domain-with-github-pages/)
* [Poole Hyde](https://github.com/poole/hyde) - The theme this site is based off of.
