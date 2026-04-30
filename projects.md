---
layout: default
title: Technical Projects
---

<style>
  .project-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
    gap: 20px;
    margin-top: 20px;
  }
  .project-card {
    background: #fff;
    border-radius: 8px;
    overflow: hidden;
    box-shadow: 0 4px 12px rgba(0,0,0,0.1);
    transition: transform 0.2s;
    text-align: left;
  }
  .project-card:hover {
    transform: translateY(-5px);
  }
  .project-image {
    width: 100%;
    height: 180px; /* This restricts the giant images to a uniform height! */
    object-fit: cover;
    background: #f4f4f4; 
  }
  .project-content {
    padding: 15px;
  }
  .project-content h3 {
    margin-top: 0;
    margin-bottom: 10px;
    font-size: 1.2em;
    color: #155799;
  }
  .project-content p {
    font-size: 0.9em;
    color: #555;
    margin: 5px 0;
  }
</style>

## Technical Projects
Here is a selection of my hardware and firmware engineering work, including university projects and hackathon prototypes.

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
