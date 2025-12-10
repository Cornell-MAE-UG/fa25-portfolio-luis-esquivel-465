---
layout: default
title: Projects
permalink: /projects/
---

## Projects

Here are some of my engineering projects:

<div class="projects-grid">
{% for project in site.projects %}
  <article class="project-card">
    <a href="{{ project.url | relative_url }}">
      {% if project.image %}
      <img src="{{ project.image | relative_url }}" alt="{{ project.title }}">
      {% endif %}
      <h3>{{ project.title }}</h3>
    </a>
    <p>{{ project.description }}</p>
  </article>
{% endfor %}
</div>

