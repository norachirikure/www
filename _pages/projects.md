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

<div class="projects">
  {% if site.enable_project_categories and page.display_categories %}
    {% for category in page.display_categories %}
    <h2 class="category">{{ category }}</h2>
    {% assign category_projects = site.projects | where: "category", category | sort: "importance" %}
    {% if page.horizontal %}
      <div class="container">
        <div class="row row-cols-1 row-cols-md-2">
        {% for project in category_projects %}
          {% include projects.liquid %}
        {% endfor %}
        </div>
      </div>
    {% else %}
      <div class="grid">
        {% for project in category_projects %}
          {% include projects.liquid %}
        {% endfor %}
      </div>
    {% if page.horizontal %}
      <div class="container">
        <div class="row row-cols-1 row-cols-md-2">
        {% for project in site.projects %}
          {% include projects.liquid %}
        {% endfor %}
        </div>
      </div>
    {% else %}
      <div class="grid">
        {% for project in site.projects %}
          {% include projects.liquid %}
        {% endfor %}
      </div>
    {% endif %}
  {% endif %}
</div>
