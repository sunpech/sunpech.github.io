---
layout: post
title: A C# Code Solution for FizzBuzz
date: '2008-09-15T22:20:00.000-05:00'
author: Steven Suwatanapongched
tags:
- Software Development
modified_time: '2012-01-01T23:03:53.750-06:00'
blogger_id: tag:blogger.com,1999:blog-6841384.post-1087262992477565695
blogger_orig_url: http://www.sunpech.com/2008/09/c-code-solution-for-fizzbuzz.html
redirect_from: /2008/09/c-code-solution-for-fizzbuzz.html
---

I read a <a href="http://it.slashdot.org/article.pl?sid=08/09/15/0210235">slashdot article</a> earlier today which lead me to a Coding Horror article: <a href="http://www.codinghorror.com/blog/archives/000781.html">Why Can't Programmers.. Program?</a>.  This lead me to the FizBuzz problem, which prompted me to write my own quickie solution in C# (as a console application).

### Problem:

<i>Write a program that prints the numbers from 1 to 100. But for multiples of three print "Fizz" instead of the number and for the multiples of five print "Buzz". For numbers which are multiples of both three and five print "FizzBuzz". </i>

#### My Quick Solution:

<pre style="font-family: Andale Mono, Lucida Console, Monaco, fixed, monospace; color: #000000; background-color: #eee;font-size: 12px;border: 1px dashed #999999;line-height: 14px;padding: 5px; overflow: auto; width: 100%"><code>for (int i = 1; i &lt;= 100; i++)

{

    if ((i % 3 == 0) &amp;&amp; (i % 5 == 0))

    {

        Console.WriteLine(&quot;FizzBuzz&quot;);

    }

    else if (i % 3 == 0)

    {

        Console.WriteLine(&quot;Fizz&quot;);

    }

    else if (i % 5 == 0)

    {

        Console.WriteLine(&quot;Buzz&quot;);

    }

    else

    {

        Console.WriteLine(i.ToString());

    }

    }

    Console.ReadLine();

</code></pre>

I know my version is probably not optimal, nor is it the shortest way to write it.  I just wanted to write it for fun, code for fun.  I honestly can't remember the last time I coded something purely for fun.  Now I'm wondering how I can optimize this in C# and even how to write it in other languages.

Where I formatted my C# code into HTML for Blogspot: <a href="http://formatmysourcecode.blogspot.com">http://formatmysourcecode.blogspot.com</a>