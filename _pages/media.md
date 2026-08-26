---
layout: page
permalink: /media/
title: Media
description: Press coverage and recognition of my research, grouped by paper.
nav: true
nav_order: 3
---

<!-- Content lives in _data/media.yml. Add coverage there, not here. -->

<div class="media-page">
  {% for paper in site.data.media %}
    {% assign coverage = paper.coverage | sort: 'date' | reverse %}
    <section class="media-group" id="{{ paper.key }}">
      <h2 class="media-paper-title">
        {% if paper.link %}
          <a href="{{ paper.link }}" target="_blank" rel="noopener noreferrer">{{ paper.title }}</a>
        {% else %}
          {{ paper.title }}
        {% endif %}
      </h2>

      <ul class="media-list">
        {% for mention in coverage %}
          <li>
            <div class="media-meta">
              <span class="outlet">{{ mention.outlet }}</span>
              <span class="date">{{ mention.date | date: '%B %Y' }}</span>
            </div>
            <a class="media-headline" href="{{ mention.url }}" target="_blank" rel="noopener noreferrer">{{ mention.headline }}</a>
            {% if mention.byline %}<span class="byline">by {{ mention.byline }}</span>{% endif %}
            {% if mention.note %}<div class="media-note">{{ mention.note }}</div>{% endif %}
          </li>
        {% endfor %}
      </ul>
    </section>
  {% endfor %}
</div>
