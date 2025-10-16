---
layout: page
title: Random
permalink: /random/
nav: true
nav_order: 70
photos:
- path: assets/img/random/kayaking.jpg
  caption: Kayaking on the Hudson
- path: assets/img/random/bigsky.jpg
  caption: Skiing @ Big Sky
- path: assets/img/random/miami.jpg
  caption: Miami
- path: assets/img/random/vitalbk.jpg
  caption: Climbing @ Vital Brooklyn
- path: assets/img/random/boston.jpg
  caption: Boston
- path: assets/img/random/vegas.jpg
  caption: Horseshoe Bend
- path: assets/img/random/dc.jpg
  caption: Washington DC
- path: assets/img/random/philly.jpg
  caption: Philly
- path: assets/img/random/bentonville.jpg
  caption: Bentonville
---

<style>
  /* Make each tile a consistent smaller width for a chill masonry grid */
  .grid-photos {
    margin-left: auto;
    margin-right: auto;
  }
  .grid-photos .grid-item {
    width: 280px; /* adjust to taste: 180-260px */
  }
  .grid-photos .caption {
    color: var(--global-text-color-light);
  }
</style>

<div class="grid grid-photos mt-4">
  {% for p in page.photos %}
    <div class="grid-item mb-3">
      {% include figure.liquid path=p.path class="img-fluid rounded z-depth-1" zoomable=true caption=p.caption sizes="220px" %}
    </div>
  {% endfor %}
  
</div>
