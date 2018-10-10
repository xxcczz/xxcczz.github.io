{% for post in paginator.posts %}
    <a href="{{ post.url }}">{{ post.title }}</a>
{% endfor %}

{% if paginator.previous_page %}
<a src="{{ paginator.previous_page_path }}"></a>
{% endif %}
