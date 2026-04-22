---
layout: default
title: Calendar
---

{% assign future_events = site.events
                        | where_exp: "event", "event.date >= site.time"
                        | sort: "date" %}
<h1>Future Events</h1>
<ul>
  {% for event in future_events %}
    <li>
      <h2>
			{% include event_link.html %}
			</h2>
      {{ event.excerpt }}
    </li>
  {% endfor %}
</ul>

{% assign past_events = site.events
                        | where_exp: "event", "event.date < site.time"
                        | sort: "date"
												| reversed %}
<h1>Past Events</h1>
<ul>
  {% for event in past_events %}
    <li>
      <h2>
			{% include event_link.html %}
			</h2>
      {{ event.excerpt }}
    </li>
  {% endfor %}
</ul>
