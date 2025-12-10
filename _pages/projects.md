---
layout: default
title: Projects
permalink: /projects/
---

## Projects

Here are some of my engineering projects:

{% for project in site.projects %}
### [{{ project.title }}]({{ project.url | relative_url }})

{{ project.description }}

{% if project.image %}
![{{ project.title }}]({{ project.image | relative_url }}){: .inline-image-r style="width: 220px"}
{% endif %}

---

{% endfor %}
