---
layout: default
title: Home
---

NIATM (Northern Illinois Association of Teachers of Mathematics)
Associate Affiliate of the National Council of Teachers of Mathematics
Serving Winnebago, Boone, and other counties in northern Illinois.

Dinner meetings are scheduled throughout the school year as well as an annual mathematics competition for area high schools.

We invite you to take a look at our site and consider joining us for a dinner meeting. Consider joining our organization.

# Explore our site

NIATM is a great way to  interchange views regarding the teaching of mathematics and related disciplines, and to further the study of problems relating to the teaching of mathematics and computer science.

- NIATM is an approved provider of Continuing Professional Development Units (CPDU).   Each presentation = 1 CPDU  

# Upcoming Events
<ul>
{% assign future_events = site.events
                        | where_exp: "event", "event.date > site.time"
												| sort: "date" %}
{% for event in future_events reverse limit:2 %}
   <li>{% include event_link.html %}</li>
{% endfor %}
</ul>


# TODO Membership
- Send Membership Dues and Dinner Meeting reservations to:
  - NIATM
  - c/o Amanda Harvey 
  - Byron High School Math Department
  - 696 N. Colfax Street
  - Byron, IL  61010
- Email:  AHarvey@byron226.org

# Membership Form
Download Word form at: [Membership Form](/assets/files/NIATMmembershipForm.docx)
