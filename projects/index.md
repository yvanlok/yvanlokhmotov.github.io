---
layout: page
title: Projects
permalink: /projects/
---

A collection of my machine learning and software development projects, primarily focused on Formula 1 data analysis and predictive modeling.

---

{% assign project_pages = site.pages | where_exp: "page", "page.path contains 'projects/'" | where_exp: "page", "page.path != 'projects/index.md'" | sort: "date" | reverse %}

{% for project in project_pages %}

<div class="project-item" markdown="1">

### [{{ project.title }}]({{ project.url }})

{{ project.summary | default: project.excerpt | strip_html | truncatewords: 30 }}

{% if project.tags and project.tags.size > 0 %}

<div class="tags">
  {% for tag in project.tags %}
  <span class="tag">{{ tag }}</span>
  {% endfor %}
</div>
{% endif %}

[View Details →]({{ project.url }})

</div>
{% endfor %}
