---
title: "STAR meetings archive"
redirect_from:
  - /central/meetings/archives.php/
---

<nav class="year-jump" aria-label="Jump to year" markdown="0">
  <span class="year-jump-label">Jump to:</span>
  {%- for y in site.data.meetings %}
  <a href="#y{{ y.year }}">{{ y.year }}</a>
  {%- endfor %}
</nav>

<div class="meeting-years" markdown="0">
{%- for y in site.data.meetings %}
  <section class="meeting-year" id="y{{ y.year }}">
    <h2 class="meeting-year-title">{{ y.year }}</h2>
    <ul class="meeting-list">
    {%- for m in y.items %}
      <li>
        <a href="{{ m.u | escape }}" target="_blank" rel="noopener">{{ m.t | escape }}</a>&nbsp;<span data-feather="external-link"></span>
        {%- if m.u2 %}
        <span class="meeting-extra">(<a href="{{ m.u2 | escape }}" target="_blank" rel="noopener">{{ m.l2 | escape }}</a>&nbsp;<span data-feather="external-link"></span>)</span>
        {%- endif %}
      </li>
    {%- endfor %}
    </ul>
  </section>
{%- endfor %}
</div>
