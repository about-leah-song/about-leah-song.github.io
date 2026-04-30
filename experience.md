---
layout: default
title: Professional Experience
---

## Professional Experience

{% for job in site.experience %}
* [**{{ job.title }}**]({{ job.url }}) — *{{ job.role }}*
  *<br>{{ job.dates }}*
{% endfor %}
