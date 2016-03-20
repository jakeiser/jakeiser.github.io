---
layout: default
title: Blog
group: "navigation"
permalink: /blog/
---

  <ul class="post-list">
    {% for post in site.posts %}
      <li>
        <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>

        <h2>
          <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
        </h2> 
        
            <p class="post-excerpt">
            {% if post.content contains '<!--excerpt.start-->' and post.content contains '<!--excerpt.end-->' %}
            {{ ((post.content | split:'<!--excerpt.start-->' | last) | split: '<!--excerpt.end-->' | first) | remove: '<p>' | remove: '</p>' }}
            {% else %}
            {{ post.content }}
            {% endif %}
            
            {% if post.content contains '<!--excerpt.end-->' %}
        	.&nbsp;.&nbsp;.&nbsp;<a href="{{ post.url | prepend: site.baseurl }}">Read more</a>
            {% endif %}
            </p>
            
      </li>
    {% endfor %}
  </ul>

  <p class="rss-subscribe">subscribe <a href="{{ "/feed.xml" | prepend: site.baseurl }}">via RSS</a></p>