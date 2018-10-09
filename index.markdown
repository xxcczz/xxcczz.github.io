---
layout: default
title: 首页标题
---
<ul>
	{% for post in site.post1s %}
	<li>

		<a href="{{ post.url }}">{{ post.title }}</a>

	</li>
	{% endfor %}
</ul>