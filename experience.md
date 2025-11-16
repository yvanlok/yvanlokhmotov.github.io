---
layout: page
title: Experience
permalink: /experience/
---

{% capture experience_content %}
{% include experience-content.md %}
{% endcapture %}
{{ experience_content | markdownify }}
