---
layout: default
title: Schedule
navigation_weight: 2
---

# {{ page.title }}

{% assign days = site.data.schedule %}
{% for day in days %}
## {{ day.day }} ({{ day.date}})
<ul>
{% for event in day.events %}
<li>{{ event.time }}: {{ event.title }}</li>
{% endfor %}
</ul>

{% endfor %}

