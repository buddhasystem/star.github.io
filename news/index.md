---
title: "Recent news"
redirect_from:
  - /central/news/
---
{% for post in site.posts %}
<h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
<p class="news-date">{{ post.date | date: "%B %-d, %Y" }}</p>
{{ post.content }}
{% endfor %}
