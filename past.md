---
layout: page
title: Past Events
permalink: /past/
---
<ul>
  {% assign TodayDate = site.time | date: '%s' %}
  {% for post in site.posts%}
  {% assign EventDate = post.date | date: '%s' %}
  {% assign EventDate = post.date | date: '%s' %}
  {% if EventDate < TodayDate %}
    <li>
        <a href="{{ post.url | absolute_url }}">{{ post.title }}</a> - {{post.date | date_to_long_string }}
      </li>
  {% endif %}
  {% endfor %}
  </ul>