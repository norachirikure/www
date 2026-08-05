---
layout: page
title: projects
permalink: /projects/
description: Research projects on collective action, citizen engagement, and public goods delivery.
nav: true
nav_order: 3
display_categories: [research]
horizontal: false
---

<div class="projects">
  {% if site.projects %}
  <div class="row row-cols-1 row-cols-md-3 g-4">
    {% assign sorted_projects = site.projects | sort: "importance" %}
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
</div>
