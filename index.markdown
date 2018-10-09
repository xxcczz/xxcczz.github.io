---
layout: default
title: สืาณฑ๊ฬโ
---
<ul class="posts">
	{% for post in site.posts %}
	<li>

		<a href="{{ post.url }}">{{ post.title }}</a>

	</li>
	{% endfor %}
</ul>