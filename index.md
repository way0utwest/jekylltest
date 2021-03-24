---
layout: home
title: "SQL Saturday Home"
---
Welcome to SQL Saturday, the data platform and SQL Server community franchise for technical events.

## Events
<table>
  <thead>
        <tr>
          <th scope="col"></th>
          <th scope="col">Event Name</th>
          <th scope="col">Date</th>
        </tr>
      </thead>
      <tbody>
  {% assign TodayDate = site.time | date: '%s' %}
  {% for post in site.posts%}
  {% assign EventDate = post.date | date: '%s' %}
   {% if EventDate >= TodayDate %}
    <tr>
    <td>{{ post.thumb }}</td>
      <td><a href="{{ post.url | absolute_url }}">{{ post.title }}</a>
      </td>
      <td>{{post.date | date: '%s' }}</td>
    </tr>
   {% endif %}
  {% endfor %}
  </tbody>
</table>


You can see completed events on the [Past Events](past.html) page.


