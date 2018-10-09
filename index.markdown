---
layout: default
title: 首页标题
---
<ul class="posts1">
	{% for post in site.posts %}
	<li>

		<a href="{{ post.url }}">{{ post.title }}</a>

	</li>
	{% endfor %}
</ul>