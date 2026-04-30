---
layout: default
title: Technical Projects
---

## Technical Projects
Here is a selection of my hardware and software engineering work, including university capstones and hackathon prototypes.

<div class="project-grid">
  {% for project in site.projects %}
  <div class="project-card">
    <a href="{{ project.url }}" style="text-decoration: none; color: inherit;">
      {% if project.header.overlay_image %}
        <img src="{{ project.header.overlay_image }}" alt="{{ project.title }}" class="project-image">
      {% else %}
        <div class="project-image" style="display:flex; align-items:center; justify-content:center; color:#999; background:#eee;">📸 Image pending</div>
      {% endif %}
      <div class="project-content">
        <h3>{{ project.title }}</h3>
        <p><strong>Tools:</strong> {{ project.tools }}</p>
        <p><em>{{ project.description }}</em></p>
      </div>
    </a>
  </div>
  {% endfor %}
</div>
