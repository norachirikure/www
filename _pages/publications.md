---
layout: page
permalink: /publications/
title: writing
nav: true
nav_order: 1
---

<div class="publications">

  <h2 id="working-papers">Working Papers</h2>
  {% bibliography -f papers -q @*[keywords~="working_paper"]* %}

  <h2 id="discussion" class="mt-4">Discussion</h2>
  {% bibliography -f papers -q @*[keywords~="discussion"]* %}

  <h2 id="policy-briefs" class="mt-4">Policy Briefs</h2>
  {% bibliography -f papers -q @*[keywords~="policy"]* %}

  <h2 id="reports" class="mt-4">Reports</h2>
  {% bibliography -f papers -q @*[keywords~="report"]* %}

</div>
