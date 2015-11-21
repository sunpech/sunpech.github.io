---
layout: post
title: Software Developers and Empathy
date: '2015-09-02T09:00:00.000-05:00'
author: Steven Suwatanapongched
tags:
- Software Development
modified_time: '2015-09-02T09:00:00.000-05:00'
thumbnail: /public/images/blog/tn_ready_player_one_book.jpg
image: /public/images/blog/ready_player_one_book.jpg
description:
header-img: /public/images/headers/header_software_development.jpg
---

I recently read [a blog post](https://www.humankode.com/security/how-a-bug-in-visual-studio-2015-exposed-my-source-code-on-github-and-cost-me-6500-in-a-few-hours) about how a developer's AWS credentials was compromised through [a bug](https://github.com/github/VisualStudio/pull/64) in the Github extension in Visual Studio 2015.

I initially discovered the link via a [reddit post](https://www.reddit.com/r/programming/comments/3j4ydl/how_a_bug_in_visual_studio_2015_exposed_my_source/). If you read some of the posts before it blew up, **you'd see a lot of mean comments made.** Yes, the Internet, or specifically in this case, *redditors* can be mean to one another-- just like in real life. But posting stuff online just makes it so much easier.

### Some Mean Comments

##### Lowering your sympathy

![reddit comment](/public/images/blog/reddit_screenshot_01.jpg)

##### Calling him stupid

![reddit comment](/public/images/blog/reddit_screenshot_02.jpg)

##### Victim blaming

![reddit comment](/public/images/blog/reddit_screenshot_03.jpg)

Software developers tend to eat their own. I mean this in the sense that they will focus on the technical, and have no empathy to one another. There's so much focus on what should have been done or how this person did not do what's considered *best practices* of today.

### Expectations

When I enter payment information into a e-commerce website-- my expectation is that it is secure. Or at least secure enough if things are compromised that my credit institution will take care of it so I'm not deeply impacted.

When I see a checkbox labeled 'Private', I'm expecting it to make the associated information private, aka, not public.

**If a software or service is not doing what is expected of it, and things go wrong from that point forward, why would we blame the user?** Let's move on to my car analogy....

### Car Analogy

Imagine you have a friend, Bob, who is a an automobile mechanic and has a car. Like many people who have cars, Bob leaves a garage door remote in it. The remote is in the car because it's convenient for Bob to be able to open/close the garage door when he leaves and returns home.

Bob also has a car key that lets him remotely lock/unlock the car. The expectation is that when Bob leaves the car and pushes the lock button that the car will lock-- and vice versa when he wants to unlock the car.

Suppose Bob's car did not work as expected-- as in it did not lock when he pushes the button on the remote key. And because it didn't lock, someone was able to get in the car, figure out where he lived, and copied the functionality of the garage door remote, and then burglar Bob's house causing financial damage.

Then Bob writes a blog post sharing his experience so maybe others can learn from it. He also happens to mention that as 10+ years as a mechanic, this has never happened to him before.

Do you simply comment on how Bob shouldn't have left the garage door remote in the car because it's a security risk? How about Bob not checking first to see if the car was truly locked after pushing the button? Or should you just plain call Bob stupid and criticize him as a auto-mechanic for not knowing better?

### Final Thoughts

Any of us with any online credentials be compromised, whether they be from a cloud computing service, social media, banking, shopping, or many of the other companies out there. All it takes if for a software/service to either not perform as intended, or some security problem.

I'm not saying that software developers should be lax on security and should trust upfront any software setting from services we use. I'm not even saying that this developer is above criticism-- there's always room for improvement.

Nor am I saying that all comments/criticism is hurtful or mean. There's quite a few that does bring up why AWS doesn't have some settings cap to automatically spin down instances that go over a certain amount. It shouldn't just be spending to infinity for all accounts. Sure it's nice for Amazon for accounts to spend money, but there's certainly a lot of fraud going on out there too. *And maybe there is a setting for this, I'm not sure as there are so many options buried in the consoles.*

**I'm saying we should empathize with the developer here.** In some way, some how, you may experience
a shitty moment in life. Maybe you've already been there, maybe not. But *wouldn't you rather have a community of you peers help you up, learn from it, and move everyone forward?* As far as I know, this bug has been [patched]((https://github.com/github/VisualStudio/pull/64).

#### Links

* [How a bug in Visual Studio 2015 exposed my source code on GitHub and cost me $6,500 in a few hours](https://www.humankode.com/security/how-a-bug-in-visual-studio-2015-exposed-my-source-code-on-github-and-cost-me-6500-in-a-few-hours)
* [Bloke clicks GitHub 'commit' button in Visual Studio, gets slapped with $6,500 AWS bill](http://www.theregister.co.uk/2015/09/01/github_bug_costs_man_thousands/)
* [HackerNews thread](https://news.ycombinator.com/item?id=10149179)
* [Reddit post](https://www.reddit.com/r/programming/comments/3j4ydl/how_a_bug_in_visual_studio_2015_exposed_my_source/)
