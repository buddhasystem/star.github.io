---
title: "STAR institutions"
redirect_from:
  - /central/collaboration/institutions.php/
---

STAR is composed of {{ site.data.institutions | size }} institutes from 14 countries, with a total of 793 collaborators.

<figure class="inst-map" markdown="0">
  <img src="{{ '/assets/images/collaboration/STAR_institutions.jpg' | relative_url }}" alt="World map with the STAR institutions marked" width="526" height="368">
  <figcaption>World map with STAR institutions marked. Blue: STAR institutions (council seat); violet: affiliated institutes.</figcaption>
</figure>

## Institutions and their STAR members

<div class="institutions" markdown="0">
{%- for inst in site.data.institutions %}
  <div class="institution">
    <div class="inst-name">{{ inst.name | escape }}</div>
    {%- if inst.url %}
    <div class="inst-link"><a href="{{ inst.url | escape }}" target="_blank" rel="noopener">{{ inst.url | escape }}</a>&nbsp;<span data-feather="external-link"></span></div>
    {%- endif %}
    <div class="inst-members">{{ inst.members | escape }}</div>
  </div>
{%- endfor %}
</div>

<p class="inst-note">(*) Member is deceased.</p>
