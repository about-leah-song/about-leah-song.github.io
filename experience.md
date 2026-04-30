---
layout: default
title: Professional Experience
description: Internships, research positions, and engineering team leadership.
header_image: /assets/images/header4.jpg
---

<style>
  .job-list {
    display: flex;
    flex-direction: column;
    gap: 20px;
    margin-top: 20px;
  }
  .job-card {
    display: flex;
    background: #fff;
    border-radius: 8px;
    box-shadow: 0 4px 12px rgba(0,0,0,0.1);
    transition: transform 0.2s;
    padding: 20px;
    align-items: center; /* Centers the logo vertically with the text */
    gap: 25px;
  }
  .job-card:hover {
    transform: translateY(-5px);
  }
  
  /* Creates a neat, uniform box for the logos, even if they are different sizes */
  .job-logo-container {
    flex-shrink: 0;
    width: 100px;
    height: 100px;
    display: flex;
    align-items: center;
    justify-content: center;
    background: #f8f9fa;
    border-radius: 8px;
    padding: 10px;
  }
  .job-logo {
    max-width: 100%;
    max-height: 100%;
    object-fit: contain;
  }
  
  .job-content {
    flex-grow: 1;
    text-align: left;
  }
  .job-content h3 {
    margin-top: 0;
    margin-bottom: 5px;
    font-size: 1.5em;
    color: #155799;
  }
  .job-content h4 {
    margin: 0 0 10px 0;
    font-size: 1.1em;
    color: #333;
    font-weight: normal;
  }
  .job-content p {
    font-size: 0.95em;
    color: #666;
    margin: 0;
  }

  /* Mobile responsiveness: Stacks the logo on top of the text on small screens */
  @media (max-width: 600px) {
    .job-card {
      flex-direction: column;
      text-align: center;
    }
    .job-content {
      text-align: center;
    }
  }
</style>

My recent internships, research positions, and engineering team leadership roles.

<div class="job-list">
  <!-- This keeps the sorting logic we just added! -->
  {% assign sorted_jobs = site.experience | sort: 'order' %}
  {% for job in sorted_jobs %}
  
  <!-- Wraps the whole card in a link to the job's dedicated page -->
  <a href="{{ job.url }}" style="text-decoration: none; color: inherit; display: block;">
    <div class="job-card">
      
      <div class="job-logo-container">
        {% if job.logo %}
          <img src="{{ job.logo }}" alt="{{ job.title }} logo" class="job-logo">
        {% else %}
          <span style="color: #ccc; font-size: 0.8em; text-align: center;">No Logo</span>
        {% endif %}
      </div>
      
      <div class="job-content">
        <h3>{{ job.title }}</h3>
        <h4>{{ job.role }}</h4>
        <p><strong>Dates:</strong> {{ job.dates }}</p>
      </div>
      
    </div>
  </a>
  
  {% endfor %}
</div>
