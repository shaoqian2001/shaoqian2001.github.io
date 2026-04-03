---
layout: page
title: games
permalink: /games/
description: Game demos and projects.
nav: true
nav_order: 4
horizontal: false
---

<!-- pages/games.md -->
<div class="projects">
  {%- assign sorted_games = site.games | sort: "importance" -%}
  <!-- Generate cards for each game -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_games -%}
      {% include projects.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_games -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
</div>
