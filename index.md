---
layout: home
title: "SQL Saturday Home"
---
Welcome to SQL Saturday, the data platform and SQL Server community franchise for technical events.

## Events

## Past Events

{% for post in site.posts limit:3 %}
{% include components/post-card.html %}
{% endfor %}