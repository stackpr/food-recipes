---
layout: page
title: Recent Posts
tagline: vegetarian healthy living
---
{% include JB/setup %}

{% assign sorted_posts = (site.posts | sort: 'title') %}
<ul class="posts">
  {% for post in sorted_posts %}
  	{% unless site.JB.hide_categories contains post.category %}
  	  <li><a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  	{% endunless %}
  {% endfor %}
</ul>
