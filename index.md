---
layout: page
title: "what's new"
---
{% include JB/setup %}

<ul class="posts">
  {% for post in site.posts limit:10 %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
    {{ post.content | truncatewords:50 | strip_html }}
    <hr />
  {% endfor %}
</ul>

