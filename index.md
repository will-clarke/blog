---
layout: page
title: William Clarke's Blog
tagline: wmmc.github.io
---
{% include JB/setup %}

## Welcome!

This is where I jot down computery-related ideas about projects that I'm doing.
Hopefully something may be useful to someone...

If you want to learn more about _me_, you should go to my [colourful and narcissistic site.](http://wmmclarke.com)


#### Some of my recent posts:

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>
