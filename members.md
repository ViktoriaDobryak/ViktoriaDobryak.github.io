---
layout: default
title: Members
---

# Active Members
<ul>
  {% assign active_positions = site.data.positions | where_exp: "p", "p.holder != 'Vacant'" %}
  {% for position in active_positions %}
    {% assign member = site.members | find:"name", position.holder %}
    <li>
		    {% include member_item.html %}
    </li>
  {% endfor %}
</ul>

# Vacant Positions
<ul>
  {% assign v_positions = site.data.positions | where: "holder","Vacant" %}
  {% for position in v_positions %}
    <li>{{ position.position }}</li>
  {% endfor %}
</ul>

# Past Members
<ul>
  {% for position in site.data.past_positions %}
    {% assign member = site.members | find:"name", position.holder %}
    <li>
      {% include member_item.html %}
    </li>
  {% endfor %}
</ul>
