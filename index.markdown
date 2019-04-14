---
layout: default
title: 标题
---

Hi there, I am [怠惰]
This site is
dedicated to providing information about [me](resume.html) and [what I do](/work).

I am a screencastr at <http://haoduoshipin.com>.


<p><br /><b>My Blog:</b></p>
  <ul class="posts">
    {% for post in site.posts %}
      <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>

<p><b>Find me on:</b></p>

<ul>

<li><a href="http://c2.com/cgi/wiki?PeterWang">Wikiwikiweb</a></li>

<li><a href="http://github.com/happypeter/">Github</a></li>

</ul>
<p><br /><b>Contact Information:</b></p>

<blockquote>
欢迎所有朋友加我微信：happypeter1983
</blockquote>

