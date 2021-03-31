---
layout: page
title: Past Events
permalink: /past/
---

The data listed here is from the public historial XML records used for the Guidebook site. If you have any corrections, please feel free to submit a Pull Request or contact the webmaster with the details.

## Previous SQL Saturday Events

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