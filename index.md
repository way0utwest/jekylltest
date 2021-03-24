---
layout: home
title: "SQL Saturday Home"
---
Welcome to SQL Saturday, the data platform and SQL Server community franchise for technical events.

## Events
  {% for post in site.posts limit 4 %}
   {% if post.tags contains 'upcoming' %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
   {% endif %}
  {% endfor %}
## Past Events

<ul>
  {% for post in site.posts limit 4 %}
   {% if post.tags contains 'completed' %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
   {% endif %}
  {% endfor %}
</ul>