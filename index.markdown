---
layout: default
title: 阿呆
---
  <ul class="posts">
    {% for post in site.posts %}
      <li><a href="\xx{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>