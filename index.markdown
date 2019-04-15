---
layout: default
title: 怠惰
---
<ul class="posts">
{% for post in site.posts %}
	<li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ post.url }}">{{ post.title }}</a></li>
	 {% endfor %}
</ul>
<blockquote>
欢迎所有朋友加我qq：417902579
</blockquote>