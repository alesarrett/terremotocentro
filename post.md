---
layout: page
title: Blog
permalink: /post/
---
<ul>
{% for posts in site.posts %}
  	<li><a href="{{ posts.baseurl }}{{ posts.url }}">{{ posts.title }}</a></li>
{% endfor %}
</ul>
