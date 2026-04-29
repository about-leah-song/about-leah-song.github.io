---
layout: default
---

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

{% for project in site.projects %}
* [**{{ project.title }}**]({{ project.url }}) 
  *Tools: {{ project.tools }}*
  <br>{{ project.description }}

{% endfor %}
