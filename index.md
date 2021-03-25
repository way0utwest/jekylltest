---
layout: home
title: "SQL Saturday Home"
---
Welcome to SQL Saturday, the data platform and SQL Server community franchise for technical events. We have a list of <a href="#events">upcoming events</a> below as well as <a href="#other">other events</a> from different sources that are of interest to the data professional.

<div <div id="upcomingevents" class="page-section">
## <a name="events"></a>Events

These are the SQL Saturday events that have been scheduled.

<table cellspacing=0 class="table table-hover table-borderless table-sortable mt-3" width="100%">
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
    <td><img src="{{ post.thumb }}"></td>
      <td><a href="{{ post.url | absolute_url }}">{{ post.title }}</a>
      </td>
      <td>{{post.date | date_to_long_string }}</td>
    </tr>
   {% endif %}
  {% endfor %}
  </tbody>
</table>

You can see completed events on the [Past Events](past) page.
</div>

<div id="otherevents" class="page-section">
## <a name="other"></a>Other Events

Here are some other events that you might find interesting as a data professional:

<table cellspacing=0 class="table table-hover table-borderless table-sortable mt-3" width="100%">
  <thead>
        <tr>
          <th scope="col">Event Name</th>
          <th scope="col">Date</th>
        </tr>
  </thead>
  <tbody>
        {% for block in site.data.otherevents.events %}
        <tr>
          <th scope="col"><a href="{{ block.url }}">{{ block.title }}</a></th>
          <th scope="col">{{ block.date }}</th>
        </tr>
        {% endfor %}
  </tbody>

</div>