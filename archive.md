---
layout: page
title: Archive
navigation: true
permalink: archive/
header-img: public/images/header_book_stacks.jpg
---

{% for post in site.posts %}
  * {{ post.date | date_to_string }} &raquo; [ {{ post.title }} ]({{ post.url }})
{% endfor %}

<hr/>

{% include tag_cloud.html %}
