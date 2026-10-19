---
layout: page
title: About Us
subtitle: "Mission · Leadership · Partners"
description: "The BioHub is a planned shared bioindustrial manufacturing facility led by WPI and Massachusetts Biomedical Initiatives, funded by the Massachusetts Technology Collaborative."
permalink: /about/
redirect_from:
  - /partners/
---

<div class="split">
  <div class="split-l">Where this comes from</div>
  <div class="prose">
    <p>The Blackstone Valley is where American industry learned to work — fifty miles of mills from Worcester to Providence, and a city at the head of the river that built the machines everyone else used. WPI was founded there in 1865 on the idea that theory and practice belong in the same building.</p>
    <p>Biology is now a manufacturing technology, and the same problem has returned: the science is ready and the infrastructure is not. The BioHub is shared pilot-scale capacity at Gateway Park, so a company with a working process can scale it here.</p>
    <p><strong>Same river. Same ethos. New century.</strong></p>
  </div>
</div>

<div class="mission">
  <h2>Mission</h2>
  <p class="pillars"><span>Infrastructure</span><span>Innovation</span><span>Workforce</span></p>
  <p>The BioHub gives companies in Central Massachusetts shared access to the equipment, process development, and trained people to run fermentation at pilot scale — so bioindustrial products invented at the bench can be made here, and bioindustrial companies can start and grow here.</p>
</div>

<div class="split">
  <div class="split-l">Vision</div>
  <div class="prose">
    <p>A Central Massachusetts where a bioindustrial company never has to leave to scale.</p>
  </div>
</div>

<h2>Leadership</h2>

<div class="people">
{%- for p in site.data.people %}
  <div class="person">
    <h3>{{ p.name | escape }}</h3>
    <p class="role">{{ p.role | escape }}</p>
    <p class="aff">{{ p.aff | escape }}</p>
  </div>
{%- endfor %}
</div>

<h2>Partners</h2>
<p class="lead">The WPI–MBI BioHub is led by an anchor partnership between WPI and Massachusetts Biomedical Initiatives, with foundational support from the Massachusetts Technology Collaborative. More than {{ site.data.facts.network_partners }} organizations across industry, academia, and government support the BioHub.</p>

<div class="cards">
{% for p in site.data.partners %}
  {% include partner-card.html partner=p %}
{% endfor %}
</div>

<div class="cta-row">
  {% include inquiry.html label="Talk to us about partnering →" interest="partnership" project="optional" %}
</div>

<h2>Governance</h2>
<p class="lead">The BioHub is governed by a <strong>Governing Board</strong> made up of WPI, MBI, MassTech, and stakeholders, supported by an <strong>Advisory Group</strong> providing strategic and technical guidance from across industry, academia, and government.</p>
