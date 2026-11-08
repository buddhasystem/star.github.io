---
title: "STAR organization"
redirect_from:
  - /central/collaboration/organization.php/
---

## Leadership

<div class="org-groups" markdown="0">
{%- for g in site.data.organization.leadership %}
  <section class="org-group">
    <h3 class="org-group-title">{{ g.group | escape }}</h3>
    <div class="org-roles">
    {%- for r in g.roles %}
      <div class="org-role">
        <div class="org-role-title">{{ r.role | escape }}</div>
        <div class="org-role-name">{{ r.name | escape }}</div>
      </div>
    {%- endfor %}
    </div>
  </section>
{%- endfor %}
</div>

<p class="org-link"><a href="https://drupal.star.bnl.gov/STAR/public/smd/organization" target="_blank" rel="noopener">Detailed organization information</a>&nbsp;<span data-feather="external-link"></span></p>

## Committees

<p class="org-link"><a href="http://drupal.star.bnl.gov/STAR/public/smd/stc" target="_blank" rel="noopener">STAR Talks committee</a>&nbsp;<span data-feather="external-link"></span></p>

## STAR Council

<p class="org-link"><a href="http://www.star.bnl.gov/public/council/coun_toc.html" target="_blank" rel="noopener">STAR Council page</a>&nbsp;<span data-feather="external-link"></span></p>

Each council seat is held by one representative, who in some cases also speaks for other institutions.

<div class="council" markdown="0">
{%- for c in site.data.organization.council %}
  <div class="council-row">
    <div class="council-inst">
      <div class="council-inst-name">{{ c.inst | escape }}</div>
      {%- if c.also %}
      <div class="council-also"><span>Also represents:</span> {{ c.also | escape }}</div>
      {%- endif %}
    </div>
    {%- if c.rep %}
    <div class="council-rep">{{ c.rep | escape }}</div>
    {%- else %}
    <div class="council-rep council-rep-none">&mdash;</div>
    {%- endif %}
  </div>
{%- endfor %}
</div>

## Junior members

<div class="council" markdown="0">
{%- for j in site.data.organization.juniors %}
  <div class="council-row">
    <div class="council-inst"><div class="council-inst-name">Junior member</div></div>
    <div class="council-rep">{{ j | escape }}</div>
  </div>
{%- endfor %}
</div>
