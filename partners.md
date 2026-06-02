---
layout: page
title: Partners
subtitle: "Academic · Industry · Public sector"
description: "The BioHub is led by WPI and Massachusetts Biomedical Initiatives and funded by the Massachusetts Technology Collaborative."
permalink: /partners/
---

The BioHub is led by an anchor partnership between WPI and Massachusetts Biomedical Initiatives, with foundational support from the Massachusetts Technology Collaborative. We're actively expanding the BioHub partner network across industry, academia, and government — full network listings are coming soon.

<div class="cards">
{% for p in site.data.partners %}
  {% include partner-card.html partner=p %}
{% endfor %}
</div>

<hr/>

<div class="card" markdown="1">

## Join the BioHub
We're looking for industry, academic, and equipment partners across the bioindustrial ecosystem. [Get in touch]({{ '/contact/' | relative_url }}) to talk through fit.

</div>
