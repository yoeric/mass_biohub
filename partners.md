---
layout: page
title: Partners
subtitle: "Academic · Industry · Public sector · Community"
permalink: /partners/
---

<a class="button" href="{{ '/contact/' | relative_url }}">Join the BioHub</a>

<div class="cards">
{% for p in site.data.partners %}
  {% include partner-card.html partner=p %}
{% endfor %}
</div>

<hr/>

## Work with us
- **Access:** shared facility use + training
- **Collaboration:** sponsored projects, joint R&D
- **Programs:** workforce development, demonstrations, testbeds
