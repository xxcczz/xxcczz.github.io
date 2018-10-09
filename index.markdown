---
layout: default
title: 首页标题
---
<ul>
    {% for post1 in site.posts %}
    <li>

        <a href="{{ post1.url }}">{{ post1.title }}</a>

    </li>
    {% endfor %}
</ul>