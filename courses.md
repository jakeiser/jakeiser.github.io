---
layout: page
title: Courses
permalink: /courses/
---

{% for page in site.pages %}
  {% if page.courses %}
   <h3><a href="{{ page.url }}">{{ page.title }}</a></h3>
  {% endif %}
{% endfor %}