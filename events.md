---
layout: default
title: Calendar
---

<h1>All Events</h1>

<ul>
  {% for event in site.events %}
    <li>
      <h2>
			{% include event_link.html %}
			</h2>
      {{ event.excerpt }}
    </li>
  {% endfor %}
</ul>
