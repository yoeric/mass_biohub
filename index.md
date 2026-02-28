---
layout: page
title: "Driving the Bioindustrial Manufacturing Revolution in Central Massachusetts"
permalink: /
---

<p class="lead">
  We are bringing together a community of partners to solve the biggest challenges in bioindustrial manufacturing.
  Our facilities support process innovation, scale-up, strain optimization, and workforce development.
</p>

<div class="cta-row">
  <a class="button" href="{{ '/about/' | relative_url }}">Mission</a>
  <a class="button" href="{{ '/facilities/' | relative_url }}">Explore facilities</a>
  <a class="button button-secondary" href="{{ '/partners/' | relative_url }}">Partner with us</a>
</div>

## What we do
<div class="cards">
  <div class="card">
    <h3 class="h3">De-risk scale-up</h3>
    <p>Process development capabilities, scale-down models, and scale-up execution readiness.</p>
  </div>
  <div class="card">
    <h3 class="h3">Enable builders</h3>
    <p>Hands-on spaces and training for prototyping, instrumentation, and practical biomanufacturing skills.</p>
  </div>
  <div class="card">
    <h3 class="h3">Accelerate innovation</h3>
    <p>High-throughput workflows for biological design-build-test-learn cycles.</p>
  </div>
</div>


<div class="hero-card">
  <h2 class="h3">Latest news</h2>
  {% assign items = site.data.news | sort: "date" | reverse | slice: 0, 3 %}
  {% if items.size > 0 %}
    <ul class="clean-list">
      {% for n in items %}
        {% include news-item.html item=n %}
      {% endfor %}
    </ul>
    <p><a href="{{ '/news/' | relative_url }}">All news →</a></p>
  {% else %}
    <p class="muted">No news yet.</p>
  {% endif %}
</div>
