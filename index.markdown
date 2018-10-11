---
layout: default
title: 阿呆
---
{% for post in paginator.posts %}
    {{ post.url }}
{% endfor %}

{% if paginator.previous_page %}
<a src="{{ paginator.previous_page_path }}"></a>
{% endif %}
