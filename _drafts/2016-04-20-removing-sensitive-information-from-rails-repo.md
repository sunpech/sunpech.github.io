---
layout: post
title: Removing Sensitive Information from a Rails Git Repository
date: '2016-04-20T09:00:00.000-05:00'
author: Steven Suwatanapongched
tags:
- Guide
- Software Development
modified_time: '2016-04-20T09:00:00.000-05:00'
thumbnail: /public/images/blog/tn_ruby-on-rails.jpg
image: /public/images/blog/ruby-on-rails.jpg
description: How to remove sensitive information such as passwords and secrets from a Ruby on Rails git repository history.
header-img: /public/images/headers/software_development.jpg
---

I have some old side projects that I initially started for fun by throwing it together quickly. At the time, I committed the work into a git repository for versioning-- a good practice, but I would also commit sensitive information such as passwords, usernames, and other secrets into config files for sake of fast deployment.

It was never my intention to release any of these project repos publicly, but after reading about [source code getting published because of a bug](https://www.humankode.com/security/how-a-bug-in-visual-studio-2015-exposed-my-source-code-on-github-and-cost-me-6500-in-a-few-hours), I decided that I didn't want to depend on software or services working as how I would hope they would.

I wanted to clean up ally my repos, Rails projects in particular, that contained any sensitive information. If you were like me with some of your project commits, I hope these steps can help you.

## Sample .gitignore

Starting with a good gitignore file will go a long way.

## Figaro gem

## Removing Sensitive information with filter-branch

### Resources

* [sample gitignore](https://github.com/github/gitignore/blob/master/Rails.gitignore)
* [figaro gem](https://github.com/laserlemon/figaro)
* [Remove sensitive data](https://help.github.com/articles/remove-sensitive-data/)
