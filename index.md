---
title: "The STAR Collaboration"
math: true
---
{% include stub.html legacy="/" note="Home page: the STAR Focus feature, the right-hand columns and the news and events feeds are placeholders until migrated." %}

## STAR Focus

<div class="focus-feature" markdown="0">

<h3>STAR focus: Measurement of Two-Point Energy Correlators Within Jets in \(p\) + \(p\) Collisions at \(\sqrt{s}\) = 200 GeV</h3>

<p>During a high-energy collision of protons, such as those at the Relativistic Heavy-Ion Collider (RHIC) and Large Hadron Collider (LHC), hard scatterings between partons within the protons can occur, resulting in large transfers of momentum. This results in partons leaving the collision with high transverse momenta (\(p_{\rm T}\)) and virtualities. In vacuum, this virtuality is shed via splitting, resulting in a parton shower that terminates in confinement of the partons into hadrons (hadronization). The final-state hadrons can be clustered into objects called jets using jet-finding algorithms. Jet substructure observables derived from jet constituents provide access to information related to the parton shower and hadronization. One such observable is the \(N\)-point energy correlator, which describes energy flow among \(N\) particles as a function of an angular scale between them, \(R_{L}\). The two-point correlator (EEC) distribution is expected to be separated into three regimes: i) the free diffusion of hadrons at small angles, ii) the perturbative evolution of the parton shower at large angles, and iii) the transition region between them. This results in the EEC distribution scaling linearly with \(R_{L}\) at small angles and \(\propto 1/{R_{L}}^{1-\gamma_2}\) at large angles, where \(\gamma_2\) is the anomalous dimension governing the EEC, a quantity defined directly by QCD. Measurement of the EEC by STAR was recently published in <a href="https://journals.aps.org/prl/abstract/10.1103/wv2t-dkgn" target="_blank" rel="noopener">PRL</a>.</p>

<figure class="focus-figure">
  <div class="focus-figure-images">
    <img src="{{ '/assets/images/focus/EEC_pp/Figure2_R0p6.png' | relative_url }}" alt="Corrected distributions of the normalized EEC within jets, differential in the average jet pT times R_L, for R_jet = 0.6 and several jet pT selections">
    <img src="{{ '/assets/images/focus/EEC_pp/ChargeRatio_R0p6.png' | relative_url }}" alt="Charge-selected EEC ratio for R_jet = 0.6 and jet pT between 20 and 30 GeV/c, compared with PYTHIA 8 Detroit Tune and HERWIG 7">
  </div>
  <figcaption><strong>Figure</strong>: (Left) Corrected distributions of the normalized EEC within jets, differential in \(\left\langle p_{\rm T,jet} \right\rangle R_{L}\) at \(R_{\rm jet} =\) 0.6 for several \(p_{\rm T, jet}\) selections. Each distribution is normalized to integrate to one in \(R_{L}\). (Right) The charge-selected EEC ratio for \(R_{\rm jet}\) = 0.6 with a jet transverse momentum selection of 20 \(&lt; p_{\rm T, jet} &lt;\) 30 GeV/\(c\). Comparisons with the PYTHIA 8 Detroit Tune and the default tune of HERWIG 7 are given.</figcaption>
</figure>

<p>The location of the transition peak in the EEC is expected to be sensitive to the onset of hadronization and therefore occurs at smaller angles \(\propto \Lambda_{\rm QCD}/p_{\rm T,jet}\) for jets with higher transverse momenta (\(p_{\rm T, jet}\)), for a given initiator flavor. In the left panel of the figure, the EEC distribution is scaled by average \(p_{\rm T, jet}\) to create a distribution differential in \(\left\langle p_{\rm T,jet} \right\rangle R_{L}\). \(\left\langle p_{\rm T,jet} \right\rangle\) is the average jet momentum in a given momentum range, as determined via PYTHIA 6. Scaled as such, the peak position, characterizing the transition region, exhibits a universal scale independent of jet momentum. Details of the hadronization process are further probed via measuring the EEC in terms of hadron pairs that have like or opposite electric charge. Subtracting these two distributions forms the charge-weighted distribution. This can then be divided by the inclusive EEC to form a ratio describing the magnitude of charge correlation on a scale from \(-\)1 to 1. A value of 0 would be expected for an infinite thermal bath with equal probability to form a like-charge or opposite-charge correlation and a more negative value corresponding to increased correlation of opposite-charge pairs. At angles larger than the transition region, the slope is positive against \(R_{L}\), showing that charge becomes de-correlated at larger angles. At angles below the transition regime, the slope begins to reverse, and the ratio moves closer to zero, which reflects a charge de-correlation that is not predicted by Monte-Carlo models. This points to a charge-dependent aspect of hadronization that is not fully captured by current Monte-Carlo models, providing opportunity for further model development.</p>

<p class="focus-posted">Posted Oct 10, 2025</p>

</div>

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
