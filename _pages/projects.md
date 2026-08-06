---
layout: page
title: projects
permalink: /projects/
description: Research projects on collective action, citizen engagement, and public goods delivery.
nav: true
nav_order: 3
display_categories: [work]
horizontal: false
---

<!-- pages/projects.md -->
<div class="projects">
{% if site.enable_project_categories and page.display_categories %}
  <!-- Display projects grouped by category -->
  {% for category in page.display_categories %}
  <h2 class="category">{{ category }}</h2>
  {% assign category_projects = site.projects | where: "category", category | sort: "importance" %}
  {% capture category_projects_count %}{{ category_projects | size }}{% endcapture %}
  <div class="grid">
    {% for project in category_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endfor %}

{% else %}
  <!-- Display all projects in a single grid sorted by importance -->
  {% assign sorted_projects = site.projects | sort: "importance" %}
  <div class="grid">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
{% endif %}
</div>
