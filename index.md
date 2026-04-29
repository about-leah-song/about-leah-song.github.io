---
layout: default
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
    height: 180px;
    object-fit: cover;
    background: #f4f4f4; /* Fallback color */
  }
  .project-content {
    padding: 15px;
  }
  .project-content h3 {
    margin-top: 0;
    margin-bottom: 10px;
    font-size: 1.2em;
  }
  .project-content p {
    font-size: 0.9em;
    color: #555;
    margin: 5px 0;
  }
</style>


## About Me
Hello! I am an Electrical Engineering student at the University of British Columbia. My background spans hardware prototyping, firmware development, and power systems design. I would love any opportunity for a coffee chat to learn more about your experience and share some of my passions! 

[Download My Full Resume (PDF)](/resume.pdf)


## Skills
* **Hardware:** Altium Designer, LTspice, MATLAB, SolidWorks
* **Software:** C/C++, Python, Verilog, ARMv7
* **Protocols:** IEEE C37.118, IEC 61850 GOOSE, Modbus, PLC


## Contact
* **Email** lsong.professional@outlook.com
* **Phone Number** 778-879-3502


## Professional Experience

{% for job in site.experience %}
* [**{{ job.title }}**]({{ job.url }}) — *{{ job.role }}*
{% endfor %}


## Technical Projects

<div class="project-grid">
  {% for project in site.projects %}
  <div class="project-card">
    <a href="{{ project.url }}" style="text-decoration: none; color: inherit;">
      
      {% if project.header.overlay_image %}
        <img src="{{ project.header.overlay_image }}" alt="{{ project.title }}" class="project-image">
      {% else %}
        <div class="project-image" style="display:flex; align-items:center; justify-content:center; color:#999;">📸 Add Image in CMS</div>
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


