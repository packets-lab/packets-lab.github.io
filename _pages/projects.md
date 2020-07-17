---
layout: page
title: projects
permalink: /projects/
description:
nav: true
---

We present *packets'* research grouped in research projects. For each different strand of work, we present highlights, funding and recent publications.

<div class="card-deck projects grid">

  {% assign sorted_projects = site.projects | sort: "importance" %}

  {% for project in sorted_projects %}

  <div class="grid-item">
    <a href="{{ project.url | relative_url }}">
    <div class="card hoverable">
      {% if project.img %}
        <img src="{{ project.img | relative_url }}">
      {% endif %}
      <div class="card-body">
      {{ project.title }}
      </div>
      {% if project.footer %}
      #<div class="card-footer">
      #  <small class="text-muted">{{ project.footer }}</small>
      #</div>
      {% endif %}
    </div>
    </a>
  </div>

  {% endfor %}

</div>
