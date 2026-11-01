---
title: "Recent news"
redirect_from:
  - /central/news/
---
{% include stub.html note="Older items from the legacy home-page news feed still need to be added as posts in _posts/ (YYYY-MM-DD-title.md)." %}

{% for post in site.posts %}
<h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
<p class="news-date">{{ post.date | date: "%B %-d, %Y" }}</p>
{{ post.content }}
{% endfor %}

See also the [news archive 2004-2009]({{ '/news/archive/' | relative_url }}).
