---
layout: page
title: cv
permalink: /cv/
nav: true
nav_order: 4
cv_pdf: Nora_Chirikure_CV.pdf
---

<div class="post">

  <header class="post-header">
    {% if page.cv_pdf %}
    <div class="cv-pdf-button" style="float: right;">
      <a href="{{ page.cv_pdf | prepend: 'assets/pdf/' | relative_url }}" target="_blank" class="btn btn-sm z-depth-0" role="button">
        <i class="fa-solid fa-file-pdf"></i> Download PDF CV
      </a>
    </div>
    {% endif %}
  </header>

  <article>
    <div class="cv">
      {% if page.cv_pdf %}
        <p class="mb-4">
          The latest version of my CV can be found <a href="{{ page.cv_pdf | prepend: 'assets/pdf/' | relative_url }}" target="_blank">here</a>.
        </p>
      {% endif %}
      
      <!-- Your written CV contents go below -->
      
    </div>
  </article>

</div>
