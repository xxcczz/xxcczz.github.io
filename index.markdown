---
layout: default
title: Peter's Corner
---
<ul class="posts">
	{% for post in site.posts %}
	<li>

		<a href="{{ post.url }}">{{ post.title }}</a>

	</li>
	{% endfor %}
</ul>