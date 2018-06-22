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
<td>{% if event.link %}<a href="{{ event.link }}">{{ event.title }}</a>{% else %}{{ event.title }}{% endif %}</td>
</tr>
{% endfor %}
</table>

{% endfor %}

