---
layout: page
title: Courses
permalink: /courses/
---

{% for page in site.pages %}
  {% if page.course %}
   <h3 style="margin-bottom:0"><a href="{{ page.url }}">{{ page.title }}</a></h3>
   {{ page.location }}
  {% endif %}

<p>
 {% if page.course and page.content contains '<!--excerpt.start-->' and page.content contains '<!--excerpt.end-->' %}
  {{ ((page.content | split: '<!--excerpt.start-->' | last) | split: '<!--excerpt.end-->' | first) | prepend: '.&nbsp;.&nbsp;.&nbsp;' }}
 {% endif %}
            
 {% if page.course and page.content contains '<!--excerpt.end-->' %}
  .&nbsp;.&nbsp;.&nbsp;<a href="{{ page.url | prepend: site.baseurl }}">Read the syllabus</a>
 {% endif %}
</p>
{% endfor %}