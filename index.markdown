---
layout: default
title: ��ҳ����
---
<ul class="posts">
	{% for post in site.posts %}
	<li>

		<a href="{{ post.url }}">{{ post.title }}</a>

	</li>
	{% endfor %}
</ul>