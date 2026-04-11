#---
#title: "Projects"
#layout: categories
#author_profile: true
#taxonomy: projects
#---

---
title: "Engineering Projects"
layout: archive
permalink: /projects/
author_profile: true
---

<div class="entries-grid">
  {% for project in site.portfolio %}
    {% include archive-single.html type="grid" %}
  {% endfor %}
</div>