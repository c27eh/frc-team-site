---
layout: default
title: Home
---

<div class="linktree">
  <h1>{{ site.team_name }} <span>#{{ site.team_number }}</span></h1>
  <p class="tagline">{{ site.tagline }}</p>

  <ul class="linktree__list">
    {% for link in site.links %}
    <li><a href="{{ link.url }}">{{ link.label }}</a></li>
    {% endfor %}
  </ul>
</div>
