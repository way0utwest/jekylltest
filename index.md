---
layout: home
title: "SQL Saturday Home"
---
Welcome to SQL Saturday, the data platform and SQL Server community franchise for technical events.

## Events
<table>
  {% for post in site.posts limit 3 %}
   {% if post.tags contains 'upcoming' %}
    <tr>
      <td><a href="{{ post.url }}">{{ post.title }}</a>
      </td>
      <td>{{post.date}}</td>
    </tr>
   {% endif %}
  {% endfor %}
</table>

## Past Events

<ul>
  {% for post in site.posts limit 3 %}
   {% if post.tags contains 'completed' %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
   {% endif %}
  {% endfor %}
</ul>