---
layout: page
permalink: /publications/
title: Research Outputs
# description: publications by categories in reversed chronological order. 
years: [Working Papers, Policy Briefs, Reports, Other Writing]
nav: true
nav_order: 1
---
<div class="publications">

  <h2>Working Papers</h2>
  {% bibliography -f papers -q @*[keywords=*working_paper*]* %}

  <h2 class="mt-4">Policy Briefs</h2>
  {% bibliography -f papers -q @*[keywords=*policy*]* %}

  <h2 class="mt-4">Reports</h2>
  {% bibliography -f papers -q @*[keywords=*report*]* %}

  <h2 class="mt-4">Other Writing</h2>
  {% bibliography -f papers -q @*[keywords=*other*]* %}

</div>
