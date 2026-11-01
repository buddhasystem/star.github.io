---
title: "The STAR Collaboration"
---
{% include stub.html legacy="/" note="Home page: the STAR Focus feature, the right-hand columns and the news and events feeds are placeholders until migrated." %}

## STAR Focus

The current STAR Focus feature will appear here. See the [archive of STAR Focus features]({{ '/focus/' | relative_url }}).

## Community links

- [Spokespersons' welcome]({{ '/collaboration/welcome/' | relative_url }})
- [STAR institutions]({{ '/collaboration/institutions/' | relative_url }})
- [Phonebook](https://phonebook.sdcc.bnl.gov/star/client/){:target="_blank" rel="noopener"}
- [BUR for Runs 23-25](https://drupal.star.bnl.gov/STAR/starnotes/public/SN0793){:target="_blank" rel="noopener"}
- [STAR publication database](https://drupal.star.bnl.gov/STAR/publications/){:target="_blank" rel="noopener"}
- [Conference presentations](https://drupal.star.bnl.gov/STAR/presentations/){:target="_blank" rel="noopener"}
- [Code of conduct](https://star.rice.edu/CodeOfConduct.html){:target="_blank" rel="noopener"}

## Events

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

## Recent news

{% for post in site.posts limit:5 %}
<h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
<p class="news-date">{{ post.date | date: "%B %-d, %Y" }}</p>
{{ post.content }}
{% endfor %}

[All news]({{ '/news/' | relative_url }})
