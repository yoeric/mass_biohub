---
layout: default
title: "Building with Biology"
subtitle: "Driving the Bioindustrial Manufacturing Revolution in Central Massachusetts"
description: "Shared access to the equipment, process development, and trained people to run fermentation at pilot scale — so a product invented at the bench can be made in Central Massachusetts."
permalink: /
redirect_from:
  - /services/
---
{%- assign f = site.data.facts %}

<div class="hero">
  <div>
    <p class="eyebrow">Gateway Park · Worcester, MA</p>
    <h1>The BioHub</h1>
    <p class="descriptor">Driving the Bioindustrial Manufacturing Revolution in Central Massachusetts</p>
    <p class="lead">The BioHub will give companies in Central Massachusetts shared access to the equipment, process development, and trained people to run fermentation at pilot scale — <strong>so a product invented at the bench can be made here.</strong></p>
    <div class="cta-row">
      {% include inquiry.html label="Email the BioHub →" project="general" %}
      <a class="button button-secondary" href="{{ '/about/' | relative_url }}">About the BioHub</a>
    </div>
  </div>
  <img class="hero-mark" src="{{ '/assets/img/logos/biohub_logo_slate.png' | relative_url }}" alt="" />
</div>

<h2>What we're building</h2>
<div class="cards">
  <div class="card">
    <span class="card-i">Infrastructure</span>
    <h3>Scale your process</h3>
    <p>Screening from 100 µL to fermentation at 100 L, with process development at every step. Screening and contract fermentation run today through WPI; shared pilot capacity is in build-out.</p>
  </div>
  <div class="card">
    <span class="card-i">Innovation</span>
    <h3>Build the equipment</h3>
    <p>The MBI Builder's Lab, a 4,500 sq ft space where process-technology startups will build and test new bioprocess hardware. Build-out underway.</p>
  </div>
  <div class="card">
    <span class="card-i">Workforce</span>
    <h3>Train your team</h3>
    <p>Competency-based tracks in bioreactor operation, remote monitoring, and downstream processing. In development with Worcester-area colleges.</p>
  </div>
</div>

<h2>By the numbers</h2>

<div class="bleed bleed-tint statband">
  <div class="stats">
    <div class="stat"><span class="stat-l">MassTech award</span><span class="stat-n">${{ f.masstech_award }}M</span><p>Initial investment to launch the BioHub.</p></div>
    <div class="stat"><span class="stat-l">Federal</span><span class="stat-n">NSF BioFoundry</span><p>Part of {{ f.nsf }} in the country.</p></div>
    <div class="stat"><span class="stat-l">Network</span><span class="stat-n">{{ f.network_partners }}+</span><p>Supporting partners across industry, academia, and government.</p></div>
    <div class="stat"><span class="stat-l">Trained at BETC</span><span class="stat-n">{{ f.betc_trained }}+</span><p>Biomanufacturing professionals in its first {{ f.betc_years }} years.</p></div>
  </div>
</div>

<div class="bleed bleed-dark" id="partner">
  <div class="inner">
    <h2>Partner with us</h2>
    <p class="lead">The BioHub is in development, and partners who join now shape what gets built. We're looking for companies with a process to scale, equipment and technology partners, academic and training partners, and employers who need bioindustrial talent.</p>
    <div class="cta-row">
      {% include inquiry.html label="Talk to us about partnering →" interest="partnership" project="optional" %}
    </div>
  </div>
</div>
