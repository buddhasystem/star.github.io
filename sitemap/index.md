---
title: "Sitemap"
redirect_from:
  - /central/sitemap.php/
---
Generated from `_data/navigation.yml`: it updates itself when navigation entries are added.

{% for item in site.data.navigation %}
- <a href="{% if item.external %}{{ item.url }}{% else %}{{ item.url | relative_url }}{% endif %}">{{ item.title }}</a>{% if item.external %} (external){% endif %}
{%- if item.children %}
{%- for c in item.children %}
  - <a href="{% if c.external %}{{ c.url }}{% else %}{{ c.url | relative_url }}{% endif %}">{{ c.title }}</a>{% if c.external %} (external){% endif %}
{%- endfor %}
{%- endif %}
{% endfor %}
