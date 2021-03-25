---
layout: page
title: Past Events
permalink: /past/
---
<ul>
  {% for post in site.posts%}
  {% assign EventDate = post.date | date: '%s' %}
    <li>
        <a href="{{ post.url | absolute_url }}">{{ post.title }}</a> - {{post.date | date_to_long_string }}
      </li>
  {% endfor %}
  </ul>