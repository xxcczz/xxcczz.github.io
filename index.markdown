{% for post in paginator.posts %}
{% endfor %}

{% if paginator.previous_page %}
<a src="{{ paginator.previous_page_path }}"></a>
{% endif %}
