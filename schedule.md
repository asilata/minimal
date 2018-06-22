---
layout: default
title: Schedule
navigation_weight: 2
---

# {{ page.title }}

{% assign days = site.data.schedule %}
{% for day in days %}
## {{ day.day }} ({{ day.date}})
<table class="schedule">
{% for event in day.events %}
<tr>
<td>{{ event.time }}</td>
<td>{{ event.title }}</td>
</tr>
{% endfor %}
</table>

{% endfor %}

