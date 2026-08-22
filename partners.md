---
layout: page
title: Partners
subtitle: "Academic · Industry · Public sector"
description: "The BioHub is led by WPI and Massachusetts Biomedical Initiatives and funded by the Massachusetts Technology Collaborative."
permalink: /partners/
---

<p class="lead">The BioHub is led by an anchor partnership between WPI and Massachusetts Biomedical Initiatives, with foundational support from the Massachusetts Technology Collaborative. More than 35 organizations across industry, academia, and government support the BioHub. We add them here as each confirms how it wants to be listed.</p>

<div class="cards">
{% for p in site.data.partners %}
  {% include partner-card.html partner=p %}
{% endfor %}
  <div class="pending">More partners publish<br />as each confirms</div>
</div>

<div class="bleed bleed-dark">
  <div class="inner">
    <h2>Join the BioHub</h2>
    <p class="lead">We're looking for industry, academic, and equipment partners.</p>
    <div class="cta-row" style="margin-bottom:0">
      <a class="button" href="{{ '/contact/' | relative_url }}">Talk through fit →</a>
    </div>
  </div>
</div>
