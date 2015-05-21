---
layout: page
title: Best Stuff
navigation: true
permalink: best/
---

A list of some of the best stuff I've come across. Enjoy.

{% for page in site.pages %}
  {% if page.best == true %}
  * [ {{ page.title }} ]({{ page.url }})
  {% endif %}
{% endfor %}
