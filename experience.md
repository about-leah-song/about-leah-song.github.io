---
layout: default
title: Professional Experience
---

## Professional Experience

{% assign sorted_jobs = site.experience | sort: 'order' %}
{% for job in sorted_jobs %}
* [**{{ job.title }}**]({{ job.url }}) — *{{ job.role }}*
  *<br>{{ job.dates }}*
{% endfor %}
