---
layout: page
title: Projects
permalink: /projects/
description: Research projects where I am Principal Investigator.
nav: true
nav_order: 3
horizontal: false
---

<!-- pages/projects.md -->
<div class="projects">
  {% assign pi_projects = site.projects | where: "role", "PI" | sort: "importance" %}

  {% if pi_projects.size > 0 %}
  <a id="pi" href=".#pi">
    <h2 class="category">Principal Investigator</h2>
  </a>

  <!-- Generate cards for each project -->
  {% if page.horizontal %}
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in pi_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in pi_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
  {% endif %}
</div>

---
layout: page
title: PROMETEO
description: Predictive process monitoring in the era of data-centric AI (ERC SEED UNIBA, 2024–2025)
img: assets/img/prometeo.jpg
importance: 1
role: PI
---
