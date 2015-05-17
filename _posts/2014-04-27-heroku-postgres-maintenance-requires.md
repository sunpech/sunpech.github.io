---
layout: post
title: Heroku Postgres Maintenance Requires Manually Updating DATABASE_URL
date: '2014-04-27T08:30:00.000-05:00'
author: Steven Suwatanapongched
tags:
- Software Development
modified_time: '2014-04-29T23:29:48.433-05:00'
thumbnail: http://1.bp.blogspot.com/-vENWaWgHtA0/U1zvgEuumLI/AAAAAAABoJE/bYnxnmERa7Y/s72-c/Screen_Shot_2014-04-27_at_4_50_28_AM.jpg
blogger_id: tag:blogger.com,1999:blog-6841384.post-7339358075956505310
blogger_orig_url: http://www.sunpech.com/2014/04/heroku-postgres-maintenance-requires.html
---

Earlier this week I got an email from <a href="http://www.heroku.com/">Heroku</a> that one of my postgres databases required maintenance. This is the email:

<blockquote>bot (Heroku Support)
Apr 25 14:02
Your database HEROKU_POSTGRESQL_COLOR_URL on &lt;project_name&gt; requires maintenance. During this period, your database credentials will become read-only. Once it has completed, your database URL will have changed, but we will update your app's config variables accordingly.
This automated maintenance is a necessary part of our Starter tier plans, Dev and Basic. Should you need more control over maintenance windows, a production database (Crane or higher) offers more control over database maintenance, as we are able to schedule them in advance and provide better tools for self-served maintenance.
We expect maintenance to last just a few moments. We will update this ticket when maintenance begins, and again once it's complete.</blockquote>

I'm fine with maintenance and the short notice. I do have a <i>free plan</i> in place as it is one of my many personal projects. What I found to be interesting is the following:

<blockquote class="tr_bq"><i>Once it has completed, your database URL will have changed, but we will update your app's config variables accordingly.</i></blockquote>

I didn't even know they could update the variables of my app without me! So I login to my Heroku account and see what the new credentials are, so I can update my project and check those changes into git.

<img border="0" src="http://1.bp.blogspot.com/-vENWaWgHtA0/U1zvgEuumLI/AAAAAAABoJE/bYnxnmERa7Y/s1600/Screen_Shot_2014-04-27_at_4_50_28_AM.jpg" height="248" width="640" />

Noted, copied, and pasted. Done. The new credentials are updated in my local project as well as my project origin. At this point I haven't even checked to see if the website is even up yet. Turns out, it's not up. The app keeps crashing. I check the logs with <span style="font-family: Courier New, Courier, monospace;">heroku logs --tail</span> and find something like following repeating:

<blockquote class="tr_bq"><span style="font-family: Courier New, Courier, monospace;">2014-04-25T14:11:59+00:00 heroku[router]: at=error code=H10 desc="App crashed" method=GET path=/ host=xxx.herokuapp.com fwd= dyno= queue= wait= connect= service= status=503 bytes=<i><span style="font-size: small;">(Note: not exact error message.)</span></i></span></blockquote>

The error message is not very helpful-- yes I know the website keeps crashing, I can see that for myself! Even worse, googling it doesn't yield any results to help fix my particular issue.

My initial thought was that this was an older rails project and something was outdated or something new was pushed accidentally. So after a long time of fiddling around with not just my code, error logs, various settings, Gemfile, etc-- I notice something in the logs about a postgres connection failure with what appears to be my old credentials. I run the command <span style="font-family: Courier New, Courier, monospace;">heroku config</span> and get:

<img border="0" src="http://1.bp.blogspot.com/-wyYvlmGNB2M/U1z0dkvTZOI/AAAAAAABoJc/xbrbGtJQ-1o/s1600/Screen_Shot_2014-04-27_at_5_10_26_AM.jpg" height="194" width="640" />

This is where I noticed that the values for <span style="font-family: Courier New, Courier, monospace;">DATABASE_URL</span> had the old credentials in it, while the <span style="font-family: Courier New, Courier, monospace;">HEROKU_POSTGRESQL_COLOR_URL</span> had the new values. So I updated <span style="font-family: Courier New, Courier, monospace;">DATABASE_URL</span> with the following command:

<blockquote class="tr_bq"><span style="font-family: Courier New, Courier, monospace;">heroku pg:promote HEROKU_POSTGRESQL_COLOR_URL</span></blockquote>

See <a href="https://devcenter.heroku.com/articles/heroku-postgresql#establish-primary-db">Heroku Postgres: Establish primary DB</a>. <i>Please replace COLOR in my variables with whatever is the name/color of you database.</i>

This will update <span style="font-family: Courier New, Courier, monospace;">DATABASE_URL</span> to the new and correct credentials. After doing this my site was up and running again. This is something Heroku should have done automatically if they were going to make any changes on my behalf.

I hope this helps others, or even myself in the future!

<i><b>Update 4/29/2014:</b> A Heroku developer contacted me and looked into my problem for me. He stated that normally the DATABASE_URL will also get updated along with any changes. Although they weren't able to find out why the changes didn't propagate for me, they will monitor this kind situation in the future.</i>

