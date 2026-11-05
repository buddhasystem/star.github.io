---
title: "Events"
---

{% assign now_s = site.time | date: "%s" | plus: 0 -%}
{%- assign n_up = 0 -%}
<h3>Upcoming</h3>
<ul>
{%- for e in site.data.events %}
{%- assign end_s = e.end | date: "%s" | plus: 0 %}
{%- if end_s >= now_s %}{% assign n_up = n_up | plus: 1 %}
<li>{% if e.url %}<a href="{{ e.url }}" target="_blank" rel="noopener">{{ e.title }}</a>{% else %}{{ e.title }}{% endif %}, {{ e.dates }}{% if e.place %}, {{ e.place }}{% endif %}</li>
{%- endif %}
{%- endfor %}
{%- if n_up == 0 %}
<li>No upcoming events listed.</li>
{%- endif %}
</ul>
<h3>Past</h3>
<ul>
{%- for e in site.data.events %}
{%- assign end_s = e.end | date: "%s" | plus: 0 %}
{%- if end_s < now_s %}
<li>{% if e.url %}<a href="{{ e.url }}" target="_blank" rel="noopener">{{ e.title }}</a>{% else %}{{ e.title }}{% endif %}, {{ e.dates }}{% if e.place %}, {{ e.place }}{% endif %}</li>
{%- endif %}
{%- endfor %}
</ul>
